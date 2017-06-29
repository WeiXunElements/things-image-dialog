# things-image-selector


Example:
`NoCancelOnEscKey` is an option for determining whether to use ESC to close the dialog.

```html
<things-image-dialog id="image-dialog"
  no-cancel-on-esc-key=[[noCancelOnEscKey]]>
</things-image-dialog>
```
Receive `things-image-dialog-toggle` and open/close the dialog.
In `things-framework`, `things-dialog-manager` handles all popup events.
`event.detail` may contain the following information.

`title` mandatory
`attachmentId` mandatory
`dialogSize` optional

```js
  var event = {
    title: data.name,
    attachmentId: data.attachment_id,
    dialogSize: 'small'
  };

  this.fire('things-image-dialog-toggle', event);
```
*****
</br></br>


## Dependencies

Element dependencies are managed via [Bower](http://bower.io/). You can install that via:

    npm install -g bower

Then, go ahead and download the element's dependencies:

    bower install

## Playing With Your Element

If you wish to work on your element in isolation, we recommend that you use
[Polyserve](https://github.com/PolymerLabs/polyserve) to keep your element's
bower dependencies in line. You can install it via:

    npm install -g polymer-cli

And you can run it via:

    polymer serve

Once running, you can preview your element at
`http://localhost:8080/components/things-image-dialog/`, where `things-image-dialog` is the name of the directory containing it.
