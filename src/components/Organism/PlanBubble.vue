<template>
  <div
    px-6 py-11
    flex columns-2 gap-x-3
    shadow-top rounded-t-10
    text-sm font-bold
    class="plan-bubble"
  >
    <a href="/plan/edit" class="plan-bubble__item">
      <figure class="plan-list__item-img">
        <img src="/img/bg_plan01.png" alt />
      </figure>
      <p>
        テイクアウト
        <br />して出かけよう
      </p>
    </a>
    <a href="/plan/edit" class="plan-bubble__item">
      <figure class="plan-list__item-img">
        <img src="/img/bg_plan02.png" alt />
      </figure>
      <p>
        カフェ
        <br />アディクション
      </p>
    </a>
    <a href="/plan/edit" class="plan-bubble__item">
      <figure class="plan-list__item-img">
        <img src="/img/bg_plan03.png" alt />
      </figure>
      <p>
        静かな世界で
        <br />精神統一
      </p>
    </a>
    <a href="/plan/edit" class="plan-bubble__item">
      <figure class="plan-list__item-img">
        <img src="/img/bg_plan04.png" alt />
      </figure>
      <p>
        スイーツを
        <br />抱いて眠りたい
      </p>
    </a>
    <a href="/plan/edit" class="plan-bubble__item">
      <figure class="plan-list__item-img">
        <img src="/img/bg_plan05.png" alt />
      </figure>
      <p>
        読書と椅子さえ
        <br />あれば
        <br />何もいらない
      </p>
    </a>
    <a href="/plan/edit" class="plan-bubble__item">
      <figure class="plan-list__item-img">
        <img src="/img/bg_plan06.png" alt />
      </figure>
      <p>
        狭い部屋が
        <br />大好き
      </p>
    </a>
  </div>
</template>

<style>
.plan-bubble {
    flex-wrap: wrap;
}

.plan-bubble__item {
    position: relative;
    display: block;
    margin-bottom: 35px;
    width: calc(50% - 9px);
    height: calc(50vw - 31px);
    background: #fff;
    border-radius: 30px;
    box-shadow: 0px 0px 20.5702px rgba(0, 0, 0, 0.16);
    overflow: hidden;
}

.plan-bubble__item.active {
    background: linear-gradient(323.9deg, #FFD1DF 21.65%, #7BFFDF 92.97%);;
}

.plan-bubble__item figure {
    position: absolute;
    left: 0;
    bottom: 0;
    width: 100%;
}

.plan-bubble__item figure img {
    width: 100%;
    height: auto;
}

.plan-bubble__item p {
    position: absolute;
    left: 12px;
    top: 12px;
    color: #279698;
}
</style>

