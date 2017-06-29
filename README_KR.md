# things-image-selector


Example:
`noCancelOnEscKey`는 ESC를 사용하여 다이얼로그를 Close시킬지 여부에 대한 옵션이다.

```html
<things-image-dialog id="image-dialog"
  no-cancel-on-esc-key=[[noCancelOnEscKey]]>
</things-image-dialog>
```
`things-image-dialog-toggle`을 받아서 Dialog를 Open/Close한다.
`things-framework`에서는 `things-dialog-manger`로 모든 popup event를 처리한다.
`event.detail`에는 아래와 같은 내용이 포함될 수 있다.

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

element의 종속성은 [Bower](http://bower.io/)를 통해 관리되며, 아래의 방법을 통해 설치할 수 있다.

    npm install -g bower

그리고, 아래의 방법을 통해 실행할 수 있다.

    bower install

## Playing With Your Element

element를 독립적으로 처리하려면 [Polyserve](https://github.com/PolymerLabs/polyserve)를 사용하여 element의 bower 의존성을 유지하도록 하며, 이는 아래의 방법을 통해 설치할 수 있다.

    npm install -g polymer-cli

그리고, 아래의 방법을 통해 실행할 수 있다.

    polymer serve

element를 실행한 경우, `things-image-dialog`가 디렉토리 이름으로 포함되어 있는 `http://localhost:8080/components/things-image-dialog/`를 통해 이를 미리 확인할 수 있다. 
