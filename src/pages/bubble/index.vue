<script setup lang="ts">

</script>

<template>
  <Header />
  <div class="top-tab">
    <p class="top-tab__item">プラン</p>
    <p class="top-tab__item active">バブル</p>
  </div>
  <div text-sm class="top-main active">
    <div class="top-main-ttl">
      <h1 text-base>自分の好奇心からBubbleをつくろう</h1>
    </div>
    <div class="top-main-cont">
      <section class="main-list">
        <h2>あなたの好奇心を3つ選んでください</h2>
        <div class="sec-cont">
          <div text-xxs class="main-list__cat">
            <p>おすすめ</p>
            <p>多い</p>
            <p class="current">フード/ドリンク</p>
            <p>レジャー</p>
            <p>サービス</p>
          </div>
          <div text-xs class="main-list__cont">
            <ul>
              <li>#ビール女子</li>
              <li>#クラフトビール</li>
              <li>#仕事帰りに一杯</li>
              <li>#取りあえず生</li>
              <li>#居酒屋</li>
              <li>#ビストロ</li>
              <li>#SUNTORY</li>
            </ul>
            <p class="main-list__cont-more">もっと見る</p>
          </div>
        </div>
      </section>
      <section class="main-selected">
        <h2>選択された好奇心</h2>
        <div class="sec-cont">
          <ul>
            <li></li>
            <li></li>
            <li></li>
          </ul>
        </div>
      </section>
      <section class="main-finish">
        <h2>Bubbleのサムネイル画像を決めて終了です</h2>
        <select name="サムネイル画像">
          <option value="ピカソ風">ピカソ風</option>
          <option value="ピカソ風">ピカソ風</option>
          <option value="ピカソ風">ピカソ風</option>
          <option value="ピカソ風">ピカソ風</option>
        </select>
      </section>
      <div class="main-btn">
        <p class="main-btn__preview">プレビューで確認しよう</p>
      </div>
      <div class="main-preview">
        <figure class="main-preview__img">
          <img src="./img/img_preview.jpg" alt />
        </figure>
        <p class="main-preview__remove">
          <i class="fa-solid fa-trash-can"></i>
        </p>
      </div>
      <div text-xs class="main-btn main-btn--privacy">
        <a href>利用規約に同意して作成する</a>
      </div>
      <div class="privacy-link">
        <a href>利用規約を読む</a>
      </div>
    </div>
  </div>
</template>

<style>
.top-tab {
  display: flex;
  justify-content: center;
}

.top-tab__item {
  width: 105px;
  margin: 0 10px;
  padding: 7px 0 9px;
  @apply text-base text-center
  color: #afb9df;
  cursor: pointer;
}

.top-tab__item.active {
  padding: 7px 0;
  color: #2a295b;
  border-bottom: 2px solid #2a295b;
}

.top-main {
  display: none;
  background: #ffffff;
  box-shadow: 0px -4px 18px rgba(0, 0, 0, 0.13);
  border-radius: 40px 40px 0 0;
}

.top-main.active {
  display: block;
}

.top-main-ttl {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 80px;
  padding: 10px 20px;
}

.top-main-ttl h1 {
  text-align: center;
  color: #4b3ca7;
}

.top-main-cont {
  height: calc(100vh - 280px);
  padding: 5px 35px 35px;
  background: #eff3f9;
  overflow-y: scroll;
}

.top-main-cont section h2 {
  margin: 30px 0 3px;
}

.top-main-cont section .sec-cont {
  padding: 12px;
  background-color: #fff;
  border: 1px solid #afb9df;
  border-radius: 12px;
}

.select-finish .main-list {
  display: none;
}

.main-list__cat {
  display: flex;
  justify-content: space-between;
  padding-bottom: 9px;
}

.main-list__cat p {
  padding: 5px 0;
  color: #5fd0a7;
}

.main-list__cat p.current {
  color: #01463e;
  border-bottom: 1px solid #01463e;
}

.main-list__cont ul li,
.main-selected ul li {
  margin-top: 13px;
  padding: 9px;
  font-weight: 400;
  color: #4b3ca7;
  background: #eff3f9;
  border-radius: 10px;
}

.main-list__cont ul li.selected,
.main-selected ul li {
  font-weight: 700;
  color: #fff;
  background-color: #4b3ca7;
}

.main-selected ul li:first-child {
  margin-top: 0;
}

.main-list__cont-more {
  margin-top: 20px;
  text-align: center;
  color: #898bd3;
}

.main-selected {
  display: none;
}

.select-finish .main-selected {
  display: block;
}

.main-finish select {
  width: 100%;
  height: 42px;
  padding: 0 13px;
  color: #afb9df;
  background-color: #fff;
  border: 1px solid #afb9df;
  border-radius: 12px;
  box-sizing: border-box;
}

.main-btn {
  margin: 34px 0 26px;
  text-align: center;
}

.main-btn p,
.main-btn a {
  display: inline-block;
  width: 178px;
  line-height: 3.4rem;
  color: #fff;
  background: #279698;
  border-radius: 12px;
}

.main-btn--privacy a {
}

.main-preview {
  position: relative;
  width: 210px;
  height: 262px;
  margin: 0 auto 80px;
  background-color: #fff;
  border-radius: 28px;
  box-shadow: 0px 4px 20px rgba(0, 0, 0, 0.16);
  overflow: hidden;
}

.main-preview__img {
  display: none;
  width: 100%;
  height: 100%;
}

.main-preview__img img {
  width: 100%;
  height: 100%;
  object-fit: contain;
  object-position: bottom center;
}

.main-preview__remove {
  position: absolute;
  right: 15px;
  top: 15px;
  display: none;
  color: #5fd0a7;
}

.main-preview.active .main-preview__img,
.main-preview.active .main-preview__remove {
  display: block;
}

.privacy-link {
  text-align: center;
  color: #afb9df;
}
</style>
