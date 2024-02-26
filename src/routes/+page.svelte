<script lang="ts">
  import iconImg from "$lib/img/icon.png";
  let profileMsg: string = " ";
  const arrProfile: string[] = [
    "オープンソース愛好家",
    "キーボード愛好家",
    "新米Rustacean",
    "グリッチポップ",
  ];
  const genProfile = (): void => {
    profileMsg =
      arrProfile[Math.floor(Math.random() * arrProfile.length)];
  };
</script>

<div class="page">
  <div class="main">
    <div class="profile">
      <img src="{iconImg}" alt="icon" />
      <div>????????</div>
      <div class="profile-msg">
        {profileMsg}
      </div>
      <button on:click="{genProfile}"> </button>

      <div class="row link">
        <div>1</div>
        <div>2</div>
        <div>3</div>
        <!-- ここにクリックするとランダムで表示されるテキストを追加する -->
        <!-- DDLCのタイトル風 -->
      </div>
    </div>
  </div>
</div>

<style lang="postcss">
  /* util */

  :root {
    --icon-size: 160px;
    --btn-bg: #cbf0f3;
    --b: #aaaaaa;
  }

  .col {
    display: flex;
    flex-direction: column;
  }

  .row {
    display: flex;
    flex-direction: row;
  }

  .btn {
    appearance: none;
    height: 20px;
    width: 80px;
    background-color: var(--btn-bg);
    border-radius: 5px;
    display: block;
  }

  /* class */

  .main {
    & * {
      margin: 1rem auto;
      text-align: center;
    }
    & img {
      height: var(--icon-size);
      width: auto;
      margin: auto;
      border-radius: 50%;
    }
    & .link {
      width: 120px;
    }
  }

  .profile {
    & .profile-msg {
      height: 1rem;
      /* ??? */

      position: absolute;
      width: 54px;
      height: 45px;
      left: calc(50% - 54px / 2 + 4px);
      top: 300px;

      font-family: "Oxanium";
      font-style: normal;
      font-weight: 400;
      font-size: 36px;
      line-height: 45px;
      /* ボックスの高さと同一 */

      color: #000000;
    }
  }
</style>
