### **React란 무엇인가?**

리액트는 UI 자바스크립트 라이브러리로써 싱글 페이지 애플리케이션(SPA)의 UI를 생성하는데 집중한 라이브러리이다.
리액트는 자바스크립트에 HTML을 포함하는 JSX(JavaScript XML)이라는 간단한 문법과 단방향 데이터 바인딩을 사용하고 있다. <br>
그리고 가상 돔(Virtual DOM)이라는 개념을 사용하여 웹 애플리케이션의 퍼포먼스를 최적화한 라이브러리이다.<br>

리액트는 SPA에서 UI를 만드는 자바스크립트 라이브러리이다 보니, SPA제작을 하는 다른 프레임워크에 비해 부족한 부분이 있다.<br>
예를 들어 리액트는 페이지 전환 기능을 제공하지 않기 때문에, 리액트를 사용하여 페이지 전환을 해야 한다면, react-router와 같은 추가적인 라이브러리를 사용해야 한다.

<br>

### **React의 특징**

- 리액트는 단방향식 데이터 흐름 모델을 사용한다.
- 리액트는 가상 DOM을 사용한다.

### **React의 단점**

- 앵귤러와 같은 프레임워크와 비교하자면 리액트는 단순 라이브러리이기 때문에, 더 많은 기능을 사용하고자 한다면 Redux, Router 등 많은 의존성 모듈이 필요하다.
- 단방향 데이터 바인딩만 제공하는 것이 복잡도를 줄이기 때문에 장점이기도 하지만, 양방향 바인딩에 비해서 더 많은 양의 코드를 작성해야 하므로 불편할 수 있다.

### **리액트의 "컴포넌트 기반 아키텍쳐"의 의미**

- 리액트에서 컴포넌트는 애플리케이션 UI 구축의 기반이다. 컴포넌트 기반 시스템이 구축되면, 각각의 개별적인 구성 요소들은 `재사용이 가능`하며 `서로 독립적으로 존재`한다.
  <br>
  즉, 구성 요소간 서로 의존하지 않으며 애플리케이션의 UI 개발이 용이해진다.

<br>

### **React에서 렌더링의 동작**

- 리액트에서는 모든 컴포넌트가 렌더링 되어야 하기 때문에 렌더링이 매우 중요한 부분이다. 리액트에서 렌더링은 `render()` 함수를 통해 이루어지는데, 이 함수가 호출되면 DOM 요소를 나타내는 요소가 반환된다.

- 한번에 둘 이상의 HTML 요소를 렌더링하는 것도 가능하다. HTML 요소들을 여는 태그, 닫는 태그로 감싸면(enclosing tag) 여러 요소를 동시에 렌더링 할 수 있다.

### **React에서 상태(State)란?**

- `리액트에서 상태는 컴포넌트의 동작 및 렌더링과 같은 부분을 제어하는 데이터 또는 객체를 의미한다.`
- 상태를 이용하여, 동적이고 인터렉티브한 컴포넌트를 쉽게 개발할 수 있다.

### **React에서 props란?**

- 리액트에서 props는 프로퍼티(properties, 속성)의 줄임말로, 읽기만 가능하며(read-only) `불변성`을 지닌 요소를 의미한다.
- 애플리케이션에서 props는 부모 컴포넌트로부터 자식 컴포넌트로 전달되는 계층 구조를 따른다. 리액트는 단방향 데이터 흐름 모델을 사용하기 때문에 `반대의 경우(자식 -> 부모)는 불가능`하다.

### **state와 props의 차이**

- props는 부모 컴포넌트에서 자식 컴포넌트로 전달되는 데이터다. `props는 수정될 수 없으며` 표시 되거나 다른 값을 계산 하는데만 사용되고 `state는 컴포넌트의 생명 주기 동안 수정될 수 있는 내부 데이터`로, `다시 렌더링해도 유지`된다.

### **setState를 사용하는 이유**

- 만약 컴포넌트의 state를 `직접 변경하려고 시도한다면, 리액트는 컴포넌트를 다시 렌더링해야 하는지 알 수 있는 방법이 없지만`, setState() 메소드를 사용한다면 리액트는 `컴포넌트의 UI를 업데이트할 수 있다`.

---

<br>

> **가상 DOM이란?**

가상 DOM은 그에 대응하는 실제 DOM을 그대로 복사한 자바스크립트 객체로서, 요소 및 요소의 어트리뷰트와 프로퍼티로 구성된 노드 트리라고 할 수 있다.
<br>
리액트의 render함수를 사용하여 노드 트리가 생성되면, 데이터 모델의 변경 사항을 기반으로 이 노드 트리 즉, 가상 DOM이 업데이트 된다.

<br>

> **돔(DOM)과 가상 돔(Virtual DOM)**

우선 DOM(Document Object Model)은 웹 페이지를 이루는 태그들을 자바스크립트가 이용 할 수 있게끔 브라우저가 트리구조로 만든 객체 모델을 의미한다.<br>
DOM(Document Object Model)을 직역하자면 `문서 객체 모델`을 의미한다.
문서 객체란 html, head, body와 같은 태그들을 JavaScript가 이용할 수 있는 객체를 의미한다.

**_DOM은 HTML과 스크립트 언어(JavaScript)를 서로 이어주는 역할을 한다._**

요즘 흔히 접하는 큰 규모의 웹 애플리케이션(트위터, 페이스북)은 스크롤바를 내릴 수록 수많은 데이터가 로딩되고 각 데이터를 표현하는 요소들이 있다. <br>
요소 개수가 몇 백 개, 몇 천 개 단위로 많은 규모가 큰 웹 애플리케이션에서 DOM에 직접 접근하여 변화를 주다보면 `성능 이슈가 조금씩 발생하기 시작`한다. 즉 느려진다는 말이다.<br>
DOM자체는 빠르지만 웹브라우저 단에서 DOM 변화가 일어나면 웹브라우저가 CSS를 다시 연산하고 레이아웃을 구성하고, 페이지 렌더링 과정에서 시간이 허비되는 것이다.

**_결론적으로 속도적인 부분과 많은 일을 수행하다 버그가 발생하거나 브라우저가 죽는 일 등등의 일을 개선하고자 가상 돔이 나오게 된 것이다._**

<br>

> DOM과 가상 DOM (Virtual DOM)의 차이

- 가상 DOM을 이용하면 실제 DOM에 변화를 바로 적용하는 것보다 전체적인 프로세스를 효율적으로 수행할 수 있다.

  - "효율적이다" = 전체적인 프로세스에 드는 비용이 비교적 적다.

- 속도 차원의 문제라기 보다 연산 횟수 차원의 문제라고 할 수 있다. 우선 각각의 DOM 조작은 레이아웃 변화, 트리 변화 및 렌더링을 일으킨다.
  - `가상 DOM을 이용하지 않으면` 변화가 있을 때마다 DOM조작이 일어나고 이에 대한 연산이 수행되며 렌더링되기 때문에 변화를 적용할 때 드는 비용이 비교적 크다.
  - `가상 DOM을 이용하면` 일종의 오프라인 DOM트리에 변화들을 적용한 뒤 그 변화를 **하나로 묶어서 한번에** 실제 DOM에 전달하기 때문에 연산 횟수가 줄어들고 변화에 대한 비용이 비교적 작다.
