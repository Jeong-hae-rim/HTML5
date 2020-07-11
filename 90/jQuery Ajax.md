# jQuery Ajax

## Ajax 문법

```javascript
jQuery.ajax( url [, settings ] )
```

- 첫 번째 인자로 url이 오고, 두 번째 인자로 ajax 통신을 하기 위한 여러가지 설정들을 지정

```javascript
$.ajax({
  url: "https://fiddle.jshell.net/favicon.png",
  beforeSend: function( xhr ) {
    xhr.overrideMimeType( "text/plain; charset=x-user-defined" );
  }
})
  .done(function( data ) {
    if ( console && console.log ) {
      console.log( "Sample of data:", data.slice( 0, 100 ) );
    }
  });
```

- Setting은 Ajax 통신을 위한 옵션을 담고 있는 객체가 들어감

  - 주요 옵션

    - data

      클라이언트에서 서버로 데이터를 전송할 때 이 옵션을 사용

    - datatype

      서버가 우리에게 돌려주는 데이터를 어떤 형식으로 할 것인지 지정해주는 것

      값으로 올 수 있는 것은 xml, json, script, html

      형식을 지정하지 않으면 jQuery가 알아서 판단

    - success

      성공했을 때 호출할 콜백을 지정

      Function(PlainObject data, String textStatus, jqXHR jqWHR)

    - type

      데이터를 전송하는 방법을 지정. GET/POST 사용 가능
