# things-image-selector


Example:
`noCancelOnEscKey`는 ESC를 사용하여 다이어로그를 Close시킬지 여부에 대한 옵션이다.

```html
<things-image-dialog id="image-dialog"
  no-cancel-on-esc-key=[[noCancelOnEscKey]]>
</things-image-dialog>
```
`things-image-dialog-toggle`를 받아서 Dialog Open,Close
`things-framework`에서는 `things-dialog-manger`로 모든 popup event를 처리한다.
`event.detail`에는 아래와 같은 내용이 포함될 수 있다.

`title` 필수
`attachmentId` 필수
`dialogSize` option

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

Element dependencies are managed via [Bower](http://bower.io/). You can
install that via:

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
`http://localhost:8080/components/things-alarm/`, where `things-alarm` is the name of the directory containing it.
