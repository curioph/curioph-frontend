<template>
  <div class="suggest-plan">
    <div class="suggest-plan-ttl">
      <h2>提案されたプラン</h2>
      <div class="suggest-plan-ttl__link">
        <a href class="suggest-plan--share">
          <i class="fa-solid fa-arrow-up-from-bracket"></i>
        </a>
        <a href>
          <i class="fa-regular fa-bookmark"></i>
        </a>
      </div>
    </div>
    <div class="suggest-plan-map">
      <figure>
        <img src="/img/suggest/map.jpg" alt />
      </figure>
    </div>
    <div class="suggest-shop">
      <div class="suggest-shop__header">
        <h3>お店の名前</h3>
        <div class="suggest-shop__header-cont">
          <div class="info">
            <p>お店の情報 お店の情報お店の情報お店の情報</p>
          </div>
          <div class="img">
            <figure>
              <img src="/img/img_user01.png" alt />
            </figure>
            <figure>
              <img src="/img/img_user01.png" alt />
            </figure>
            <figure>
              <img src="/img/img_user01.png" alt />
            </figure>
          </div>
        </div>
        <p class="suggest-shop__header-like">😍</p>
      </div>
      <div class="suggest-shop__sub">
        <div class="suggest-shop__sub-item">
          <figure>
            <img src="/img/suggest/img_shop01.jpg" alt />
          </figure>
          <div class="cont">
            <h4>丸の内どうぶつ公園</h4>
            <div class="summary">
              <p>
                今だけ200円割引
                <br />天候左右なし！
                <br />夏休み企画ペンギン飼育舎体験ツアー
              </p>
            </div>
            <div class="text">
              <p>
                ペンギンを飼育している施設の中に入り、ペンギンと同じ大地に立って間近で観察できる施設です。
                <br />施設内では「フンボルトペンギン」が暮らしています。 また、ペンギン舎ではペンギンとふれあえるイベントも開催中です。飼育係がペンギンについてお話をします。また、ペンギンがエサを食べる姿をご覧になれます。ペンギンの大地に入り、餌やり体験が可能です。
              </p>
            </div>
            <div class="price">
              <p>
                <span class="regular">
                  通常価格
                  <span>¥1,400</span>
                </span>
                <span class="sale">
                  <i class="fa-solid fa-caret-right"></i>
                  <span>¥1,200</span>
                </span>
              </p>
            </div>
            <a href>詳細はこちら！</a>
          </div>
          <p class="suggest-shop__header-like">😍</p>
        </div>
        <div class="suggest-shop__sub-item">
          <figure>
            <img src="/img/suggest/img_shop02.jpg" alt />
          </figure>
          <div class="cont">
            <h4>みどり牧場</h4>
            <div class="summary">
              <p>ソフトクリーム作り体験</p>
            </div>
            <div class="text">
              <p>みどり牧場ではちょっと変わったソフトクリーム体験を紹介。自分で絞った牛乳を…テキストが入ります。シャーベットにも変更可能。なんと今回に限りいちごやレモン、チョコレートなど様々なフレーバーをご��意してお待ちしております。…テキストが入ります。</p>
            </div>
            <div class="price">
              <p>¥800</p>
            </div>
            <a href>詳細はこちら！</a>
          </div>
        </div>
      </div>
    </div>
    <div class="suggest-shop">
      <div class="suggest-shop__header">
        <h3>お店の名前</h3>
        <div class="suggest-shop__header-cont">
          <div class="info">
            <p>お店の情報 お店の情報お店の情報お店の情報</p>
          </div>
          <div class="img">
            <figure>
              <img src="/img/img_user01.png" alt />
            </figure>
            <figure>
              <img src="/img/img_user01.png" alt />
            </figure>
            <figure>
              <img src="/img/img_user01.png" alt />
            </figure>
          </div>
        </div>
        <p class="suggest-shop__header-close">×</p>
      </div>
    </div>
    <div class="suggest-shop">
      <div class="suggest-shop__header">
        <h3>お店の名前</h3>
        <div class="suggest-shop__header-cont">
          <div class="info">
            <p>お店の情報 お店の情報お店の情報お店の情報</p>
          </div>
          <div class="img">
            <figure>
              <img src="/img/img_user01.png" alt />
            </figure>
            <figure>
              <img src="/img/img_user01.png" alt />
            </figure>
            <figure>
              <img src="/img/img_user01.png" alt />
            </figure>
          </div>
        </div>
        <p class="suggest-shop__header-close">×</p>
      </div>
    </div>
    <div class="suggest-shop">
      <div class="suggest-shop__header">
        <h3>お店の名前</h3>
        <div class="suggest-shop__header-cont">
          <div class="info">
            <p>お店の情報 お店の情報お店の情報お店の情報</p>
          </div>
          <div class="img">
            <figure>
              <img src="/img/img_user01.png" alt />
            </figure>
            <figure>
              <img src="/img/img_user01.png" alt />
            </figure>
            <figure>
              <img src="/img/img_user01.png" alt />
            </figure>
          </div>
        </div>
        <p class="suggest-shop__header-close">×</p>
      </div>
    </div>
  </div>
</template>

<style>
.suggest-plan {
  position: fixed;
  left: 0;
  bottom: 0;
  width: 100%;
  max-height: calc(100vh - 95px);
  padding: 28px 22px 112px;
  border-radius: 40px 40px 0 0;
  background: linear-gradient(44.43deg, #50e1d0 8.47%, #dacdff 85.32%);
  box-shadow: 0px -4px 18px rgba(0, 0, 0, 0.13);
  overflow-y: scroll;
  z-index: 2;
}

.suggest-plan-ttl {
  display: flex;
  justify-content: space-between;
  margin-bottom: 16px;
}

.suggest-plan-ttl h2 {
  font-size: 2.2rem;
  flex: 1;
}

.suggest-plan-ttl__link {
  display: flex;
}

.suggest-plan-ttl__link a {
  display: block;
  margin-left: 20px;
  font-size: 2rem;
}

.suggest-plan-map img {
  width: 100%;
  border-radius: 20px 20px 0 0;
}

.suggest-shop {
  margin-top: 27px;
  font-family: "Noto Sans JP", sans-serif;
}

.suggest-plan-map + .suggest-shop {
  margin-top: 0;
}

.suggest-shop__header {
  position: relative;
  padding: 13px;
  background-color: #fff;
  box-shadow: 0px 3px 12px rgba(0, 0, 0, 0.08);
  border-radius: 20px;
}

.suggest-plan-map + .suggest-shop .suggest-shop__header {
  border-radius: 0 0 20px 20px;
}

.suggest-shop__header-like,
.suggest-shop__header-close {
  position: absolute;
  right: 12px;
  top: 5px;
  font-size: 2.4rem;
  line-height: 1;
}

.suggest-shop__header-like {
  right: 10px;
  font-family: "Noto Sans JP", sans-serif;
  font-size: 2.6rem;
}

.suggest-shop__header-close {
  color: #afb9df;
}

.suggest-shop__header h3 {
  margin-bottom: 10px;
  font-size: 1.2rem;
  font-weight: 900;
}

.suggest-shop__header-cont {
  display: flex;
  justify-content: space-between;
}

.suggest-shop__header-cont .info {
  width: 48%;
  font-size: 0.9rem;
  color: #898bd3;
}

.suggest-shop__header-cont .img {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  width: 48.5%;
  margin: 0 3px;
}

.suggest-shop__sub {
  margin-top: 54px;
}

.suggest-shop__sub-item {
  position: relative;
  display: flex;
  background: #fff;
  box-shadow: 0px 3px 12px rgba(0, 0, 0, 0.08);
  border-radius: 20px;
  overflow: hidden;
}

.suggest-shop__sub-item + .suggest-shop__sub-item {
  margin-top: 27px;
}

.suggest-shop__sub-item figure {
  width: 55%;
}

.suggest-shop__sub-item figure img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.suggest-shop__sub-item .cont {
  flex: 1;
  padding: 23px 12px;
}

.suggest-shop__sub-item .cont h4 {
  margin-bottom: 10px;
  padding-left: 8px;
  line-height: 1.8;
  color: #f26262;
  border-left: 2px solid #f26262;
}

.suggest-shop__sub-item .cont .summary,
.suggest-shop__sub-item .cont .text,
.suggest-shop__sub-item .cont .price {
  display: flex;
  align-items: center;
  margin-bottom: 10px;
  padding-left: 8px;
  line-height: 1.5;
  border-left: 2px solid;
}

.suggest-shop__sub-item .cont .summary {
  min-height: 28px;
  font-size: 0.7rem;
}

.suggest-shop__sub-item .cont .text {
  min-height: 43px;
  font-size: 0.5rem;
  font-weight: 400;
  color: #4b3ca7;
}

.suggest-shop__sub-item .cont .price {
  font-family: "DIN-BoldAlternate";
  font-size: 1.4rem;
  border-color: #f26262;
}

.suggest-shop__sub-item .cont .price .regular {
  font-size: 0.5rem;
}

.suggest-shop__sub-item .cont .price .regular span {
  font-size: 1rem;
  text-decoration-line: line-through;
}

.suggest-shop__sub-item .cont .price .sale {
  color: #f26262;
}

.suggest-shop__sub-item .cont a {
  display: block;
  text-align: center;
  font-size: 0.55rem;
  line-height: 16px;
  letter-spacing: 0.15px;
  color: #fff;
  background: #4b3ca7;
}
</style>
