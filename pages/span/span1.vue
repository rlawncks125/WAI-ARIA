<script setup lang="ts"></script>

<template>
  <div>span1</div>

  <!-- <button>물품추</button>
  <div role="button" tabindex="0">div 버튼</div> -->

  <!-- <span tabindex="0">스판</span>
  <span tabindex="0" aria-label="스판 label">스판</span> -->

  <!-- <a href="#">지금 페이지</a>
  <a href="#" aria-label="지금페이지 라벨">aria 페이지</a> -->

  <!-- <NuxtLink to="#">홈</NuxtLink> -->

  <!-- <div aria-labelledby="header description" tabindex="0">0</div>
  <p id="header">헤더</p>
  <p id="description">설명</p> -->

  <!-- <button aria-label="검색">🔍</button> -->

  <!-- <span aria-labelledby="today-todo" tabindex="0">오늘 할 일</span>
  <ul id="today-todo">
    <li tabindex="0">자바스크립트 공부</li>
    <li tabindex="0">html/css 과제</li>
    <li tabindex="0">알고리즘 문제풀이</li>
  </ul> -->

  <!-- <label for="input_name">이름 :</label>
  <input type="text" id="input_name" aria-describedby="name_tip" />
  <p id="name_tip" role="tooltip">한글 만 허용합니다.</p> -->

  <button aria-controls="menu-panel" aria-haspopup="true">메뉴 토글</button>
  <div>나떨어져</div>
  <div>나떨어져</div>
  <div>나떨어져</div>
  <div>나떨어져</div>
  <div>나떨어져</div>
  <div>나떨어져</div>
  <div>나떨어져</div>
  <div>나떨어져</div>
  <ul id="menu-panel" tabindex="0">
    <li>1</li>
    <li>2</li>
    <li>3</li>
    <li>4</li>
  </ul>

  <!-- <button aria-haspopup="true">더 보기</button> -->
</template>

<style lang="scss" scoped></style>
