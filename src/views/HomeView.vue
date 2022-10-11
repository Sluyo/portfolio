<script setup>
  import SideBar from '../components/sideBar.vue'
</script>

<template>
    <SideBar />
    <div class="frstThing">
      <div class="center">
        EvoCktail
      </div>
    </div>
    <div id="featured">
    <h1>FEATURED</h1>
    <div class="featuresImg">
      <div class="showing fromBottom">
        <button>Buy Now</button>
      </div>
      <img src='img/cocktail1.png' alt="test">
    </div>
    <div class="featuresImg">
      <div class="showing">
        <button>Buy Now</button>
      </div>
      <img src='img/cocktail2.png' alt="test">
    </div>
    <div class="featuresImg">
      <div class="showing fromBottom">
        <button>Buy Now</button>
      </div>
      <img src='img/kraken.png' alt="test">
    </div>
  </div>
  <div id="cocktails">
    <div class="imgPres">
      <div class="leftLink">
        <RouterLink to="/shop" class="linkTo">
          Check the 
          Cocktails
        </RouterLink>
      </div>
    </div>
    <div class="presentation">
      <div class="titlePres">
        <h1>TASTE AND ENJOY</h1>
      </div>
      <div class="rightLink">
        <RouterLink to="/shop" class="linkTo">
          Check the 
          Mocktails
        </RouterLink>
      </div>
    </div>
  </div>
  <div id="originals">
    <div class="text">
      <h1>
        Explore the Mysteries
      </h1>
      <div>
        Fed up with the regular cocktails ?<br>
        Try going deep into the original stuff.<br>
        <br>You might not come back from it.
      </div>
      <div class="originalsLink">
        <RouterLink to="" class="linkTo">
          Follow the Deep Path
        </RouterLink>
      </div>
    </div>
  </div>
  <div id="about">
    <div class="center">
      EvoCktail
      <br>2 people 1 project
    </div>
  </div>
</template>

<style scoped lang="scss">
  .frstThing {
    height: 760px;
    width: 100%;
    background-image: radial-gradient(rgba(0, 0, 0, 0.4), black 75%), url('img/bar.png');
    color: white;
    font-style: bold;
    font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;

    .center {
      position: absolute;
      top: 40%;
      left: 35%;
      font-size: 120px;
      background: -webkit-linear-gradient(rgb(149, 149, 149), rgb(63, 63, 63));
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }
  }

  #featured {
    background: linear-gradient(to bottom, black, rgba(0, 0, 0, 0.4) 100px);
    height: 760px;
    display: flex;
    flex-direction: row;
    color: white;

    h1 {
      z-index: 3;
      padding-top: 40px;
      padding-left: 50px;
      position: absolute;
    }

    .featuresImg {
      padding-top: 70px;
      width: 550px;
      height: 680px;
      background-color: none;
      text-align: center;

      .showing {
        position: absolute;
        z-index: 2;
        width: 510px;
        height: 0px;

        button {
          border: solid 2px white;
          font-size: large;
          padding: 10px;
          background: none;
          color: white;
          display: none;
          cursor: pointer;
        }

        button:hover {
          background: rgba(57, 57, 57, 0.823);
        }
      }

      .fromBottom {
        bottom: 0;
      }
    } 

    .featuresImg:hover {
      .showing {
        height: 685px;
        background-color: rgba(68, 68, 68, 0.873);
        transition: 0.3s;
        justify-content: center;

        button {
          display: block;
          margin: auto;
          margin-top: 120%;
        }
      }

      .fromBottom {
        height: 685px;
        position: absolute;
        top: 830px;
      }
    }

    img {
      width: 360px;
      height: 550px;
      padding-top: 75px;
    }  
  }

  #cocktails {
    height: 760px;
    width: 100%;
    position: relative;
    background: linear-gradient(to bottom, rgba(0, 0, 0, 0.4), black 90%);

    .imgPres {
      color: white;
      position: absolute;
      top: 0;
      left: 40px;
      width: 64%;
      height: 100%;
      background-image: url("img/kraken.png");
      background-repeat: no-repeat;
      clip-path: polygon(0 0, 100% 0%, 50% 100%, 0% 100%); 
      .toLink:hover {
        background: rgba(78, 78, 78, 0.467);
      }
    }

    .presentation {
      position: absolute;
      top: 0;
      right: 0;
      width: 64%;
      height: 100%;
      background-image: url('img/mocktail.png');
      background-repeat: no-repeat;
      background-position-x: -50px;
      clip-path: polygon(50% 0, 100% 0%, 100% 100%, 0% 100%); 

      .titlePres {
        margin-top: 100px;
        color: white;
        border: none;
      }

      h1 {
        margin: 0px 0px 0px 650px;
        width: 160px;
        padding: 20px;
        text-align: right;
      }
    }

    .linkTo {
        text-decoration: none;
        font-weight: bolder;
        font-size: 30px;
        color: white;
        width: 140px;
    }

    .leftLink {
      margin: 500px 0% 0% 250px;
      border: solid 2px white;
      width: 140px;
      padding: 20px;
      background: #5757575f;
      color: white;
      cursor: pointer;
      text-align: center;
    }

    .leftLink:hover {
      background: rgba(78, 78, 78, 0.467);
    }

    .rightLink {
      margin: 250px 0px 0px 250px;
      border: solid 2px white;
      width: 140px;
      padding: 20px;
      background: #5757575f;
      color: white;
      cursor: pointer;
      text-align: center;
    }

    .rightLink:hover {
      background: rgba(78, 78, 78, 0.467);
    }
  }

  #originals {
    height: 760px;
    width: 100%;
    background-image: linear-gradient(135deg, rgba(0, 0, 0, 0.2), rgb(0, 0, 0) 60%), url('img/shots.png');
    background-repeat: no-repeat;

    .text {
      margin: 0 100px 0 0;
      padding-top: 250px;

      h1 {
        color: white;
        text-align: right;
      }

      div {
        text-align: right;
        color: #5e5e5e;
        font-size: large;
      }

      .originalsLink {
        margin-top: 50px;
      }

      .linkTo {
        text-decoration: none;
        font-weight: bolder;
        font-size: 30px;
        color: white;
        width: 140px;
        border: solid 2px white;
        padding: 10px;
        margin-left: 1080px;
      }

      .linkTo:hover {
        background: rgba(78, 78, 78, 0.467);
      }
    }
  }

  #about {
    height: 760px;
    width: 100%;
    background-image: linear-gradient(to bottom, black, rgba(0, 0, 0, 0)), url('img/us.png');
    background-repeat: no-repeat;
    background-size: 100% 100%;

    .center {
      text-align: center;
      position: relative;
      top: 55%;
      font-size: 60px;
      background: -webkit-linear-gradient(rgb(136, 136, 136), rgb(0, 0, 0));
      text-shadow: 2px 2px white;
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }
  }
</style>

