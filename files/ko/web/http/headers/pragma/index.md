---
title: Pragma
slug: Web/HTTP/Headers/Pragma
tags:
  - Deprecated
  - HTTP
  - 삭제됨
  - 요청
  - 캐싱
  - 헤더
translation_of: Web/HTTP/Headers/Pragma
---

{{HTTPSidebar}}

HTTP/1.0 의 **`Pragma`** 헤더는 요청-응답 체인에 다양한 영향을 줄 수 있는 구현관련 헤더이다. 이것은 HTTP/1.0 버전에서 HTTP/1.1 버전의 `Cache-Control` 헤더가 생기기 전 그것과 동일한 역할을 하는 대용 헤더로 사용되었다.

> **참고:** `Pragma` 는 HTTP 응답에서 명시되지 않았던 헤더여서 일반적인 HTTP/1.1 의 `Cache-Control` 헤더의 신뢰할만한 대체재로 사용될수는 없다. 비록 그것이 응답에서 `Cache-Control` 헤더가 생략되었을 시, `Cache-Control: no-cache` 와 동일하게 효과를 주긴 하지만 말이다. `Pragma` 헤더는 HTTP/1.0 를 사용하는 클라이언트들만을 위한 비공식적인 호환성을 위해서 사용하는것이 옳다.

<table class="properties">
  <tbody>
    <tr>
      <th scope="row">Header type</th>
      <td>
        {{Glossary("General header")}}, 그러나 응답 동작은 정해지지
        않아서 구현 방식에 따른다.
      </td>
    </tr>
    <tr>
      <th scope="row">{{Glossary("Forbidden header name")}}</th>
      <td>아님</td>
    </tr>
    <tr>
      <th scope="row">
        {{Glossary("Simple response header", "CORS-safelisted response-header")}}
      </th>
      <td>맞음</td>
    </tr>
  </tbody>
</table>

## 문법

```
Pragma: no-cache
```

## 디렉티브

- no-cache
  - : `Cache-Control: no-cache` 와 같다. 캐시가 캐시 복사본을 릴리즈 하기전에 원격 서버로 요청을 날려 유효성 검사를 강제하도록 한다.

## 예제

```
Pragma: no-cache
```

## 세부사항

| Specification                                | Title                                           |
| -------------------------------------------- | ----------------------------------------------- |
| {{RFC("7234", "Pragma", "5.4")}} | Hypertext Transfer Protocol (HTTP/1.1): Caching |

## 브라우저 호환성

<p class="hidden">이 페이지의 호환성 테이블은 특정하게 구조화된 데이터를 기반으로 만들어졌다. 당신이 만일 이 데이터에 기여하고 싶다면 아래의 링크를 따라가 우리에게 Pull Request 를 보내면 된다.</p>

{{Compat("http.headers.Pragma")}}

## 그외 볼것들

- {{HTTPHeader("Cache-Control")}}
- {{HTTPHeader("Expires")}}
