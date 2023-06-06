# HTML self-closing

![image](https://github.com/littleduck1219/TIL/assets/107936957/53563af5-6e4e-4fc8-8ed2-91a351c9810c)


강의를 듣던중 태그의 마지막에 /를 붙이는 경우가 있어서 알아보았습니다.

 

에서 마지막에 `/`를 사용하는 이유는 HTML에서 self-closing 또는 void 태그를 나타내기 위해서입니다.

HTML에서 내용을 가지지 않는 태그들이 있습니다. 이러한 태그들은 열고 닫는 것이 아니라, 하나의 태그로 완전히 기술됩니다. 예를 들어, `<input>`, `<img>`, `<br>` 등과 같은 태그들입니다. 이러한 태그들은 종종 self-closing 또는 void 태그라고도 불립니다.
`/` 를 추가함으로써 태그가 자체적으로 닫힘을 명시적으로 표시하므로, HTML 문서의 명확성과 구문 분석의 용이성을 향상시킵니다.

그러나 HTML5에서는 void 태그의 경우 self-closing `/`를 사용하지 않아도 됩니다. 그래서

`<input type="text" placeholder="Write a note...">`도 유효한 구문입니다. 하지만 XML 또는 XHTML과 같이 strict syntax를 요구하는 마크업 언어에서는 `/`를 사용하여 태그를 명확하게 닫아야 합니다.
