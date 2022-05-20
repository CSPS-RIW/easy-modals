# Easy Modals

This app uses [vite](https://vitejs.dev/guide/) to bundle the scripts and styles

## First steps:

* In the terminal add: `npm install` to install all the dependencies.
* Then use `npm run dev` to run a development environment.
* To compile the scss files use `npm run sass-watch`

## Usage:

Add all your content (including the trigger-btns) inside the div with the class of `content-wrapper`.

### Copy the following structure for the triggers

```html
    <button id="trigger_1" class="btn btn-secondary trigger-btn hidden" title="Open Modal"
      data-modal="modal_1">
      Trigger #1
    </button>
```

Add the modal content inside the div with the class `modals`. This one should be outside `.content-wrapper`.

### Copy the following structure for the modals:

```html
 <dialog id="modal_1">
      <div class="modal-content">
        <div class="modal-header">
          <h2 class="add-title">Modal title</h2>
          <button title="Close overlay (escape key)" type="button"
            class="close-modal">×</button>
        </div>
        <div class="modal-body">
          <p>Modal body</p>
        </div>
        <div class="modal-footer">
          <button id="btn_close_1" class="btn btn-secondary close-modal">Close</button>
        </div>
      </div>
    </dialog>
```

Make sure that `data-modal` in the `.trigger-btn` is equal to the `id` in the dialog. This makes sure that you can add as many modals as you want in one page.

You can add as many modals as you want and as long as the `data-modal` and the `id`, match, there will not be any conflicts.

## SCSS

This project uses the Sass Module system so you won't be able to use the `@import` tag. Instead use the `@use` and `@forward` tags. Read [the Sass documentation](https://sass-lang.com/blog/the-module-system-is-launched) for more information.
