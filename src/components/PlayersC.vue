<template>
  <div>
    <!-- <div class="fifa-card">
      <div class="player-info">
        <div class="player-image">
          <img :src="player.image" :alt="player.name" />
        </div>
        <div class="player-details">
          <h2 class="player-name">{{ player.name }}</h2>
          <p class="player-club">{{ player.club }}</p>
          <p class="player-position">{{ player.position }}</p>
        </div>
      </div>
      <div class="player-rating">
        <h3 class="rating-label">FIFA Rating</h3>
        <div class="rating-value">{{ player.rating }}</div>
      </div>
    </div> -->

    <div class="container-fluid">
      <div class="row">
        <div class="col-12 col-sm- col-md-4 col-lg-4">
          <div class="card" >
          <div class="card-main">
            <div class="card-header">
              <div class="card-header-bg"></div>
              <img
                class="card-image"
                src="https://i.postimg.cc/qRvvfsbr/My-project-1.png"
                alt=""
              />
            </div>
            <h1 class="card-name">TIMOTHY</h1>
            <div class="card-attributes">
              <div class="card-attribute">
                <span class="card-attribute__value">80</span
                ><span class="card-attribute__name">PAC</span>
              </div>
              <div class="card-attribute">
                <span class="card-attribute__value">85</span
                ><span class="card-attribute__name">DRI</span>
              </div>
              <div class="card-attribute">
                <span class="card-attribute__value">82</span
                ><span class="card-attribute__name">SHO</span>
              </div>
              <div class="card-attribute">
                <span class="card-attribute__value">86</span
                ><span class="card-attribute__name">DEF</span>
              </div>
              <div class="card-attribute">
                <span class="card-attribute__value">84</span
                ><span class="card-attribute__name">PAS</span>
              </div>
              <div class="card-attribute">
                <span class="card-attribute__value">87</span
                ><span class="card-attribute__name">PHY</span>
              </div>
              <div class="card-attribute" style="margin:auto">
                <span class="card-attribute__value">87</span
                ><span class="card-attribute__name">OVR</span>
              </div>
              
            </div>
            <div class="card-overall" >
                <span class="card-attribute__value"  style="color: #f90; margin:auto">CAM/CDM</span
                >
                <!-- <span class="card-attribute__name" ></span> -->
              </div>
          </div>
        </div>

        </div>
        
        <div class="col-12 col-sm- col-md-4 col-lg-4">
          <div class="card">
          <div class="card-main">
            <div class="card-header">
              <div class="card-header-bg"></div>
              <img
                class="card-image"
                src="https://i.postimg.cc/W4K8SNhj/My-project-2.png"
                alt=""
              />
            </div>
            <h1 class="card-name">IMRAAN</h1>
            <div class="card-attributes">
              <div class="card-attribute">
                <span class="card-attribute__value">78</span
                ><span class="card-attribute__name">PAC</span>
              </div>
              <div class="card-attribute">
                <span class="card-attribute__value">75</span
                ><span class="card-attribute__name">DRI</span>
              </div>
              <div class="card-attribute">
                <span class="card-attribute__value">72</span
                ><span class="card-attribute__name">SHO</span>
              </div>
              <div class="card-attribute">
                <span class="card-attribute__value">64</span
                ><span class="card-attribute__name">DEF</span>
              </div>
              <div class="card-attribute">
                <span class="card-attribute__value">72</span
                ><span class="card-attribute__name">PAS</span>
              </div>
              <div class="card-attribute">
                <span class="card-attribute__value">71</span
                ><span class="card-attribute__name">PHY</span>
              </div>
              <div class="card-attribute" style="margin:auto">
                <span class="card-attribute__value">73</span
                ><span class="card-attribute__name">OVR</span>
              </div>
              
            </div>
            <div class="card-overall" >
                <span class="card-attribute__value"  style="color: #f90; margin:auto">ST/CAM</span
 >
                
              </div>
          </div>
        </div>

        </div>

        <div class="col-12 col-sm- col-md-4 col-lg-4">
          <div class="card">
          <div class="card-main">
            <div class="card-header">
              <div class="card-header-bg"></div>
              <img
                class="card-image"
                src="https://i.postimg.cc/dVGZgJHw/My-project-1-1-1-1.png"
                alt=""
              />
            </div>
            <h1 class="card-name">BRANDON</h1>
            <div class="card-attributes">
              <div class="card-attribute">
                <span class="card-attribute__value">85</span
                ><span class="card-attribute__name">PAC</span>
              </div>
              <div class="card-attribute">
                <span class="card-attribute__value">80</span
                ><span class="card-attribute__name">DRI</span>
              </div>
              <div class="card-attribute">
                <span class="card-attribute__value">78</span
                ><span class="card-attribute__name">SHO</span>
              </div>
              <div class="card-attribute">
                <span class="card-attribute__value">87</span
                ><span class="card-attribute__name">DEF</span>
              </div>
              <div class="card-attribute">
                <span class="card-attribute__value">74</span
                ><span class="card-attribute__name">PAS</span>
              </div>
              <div class="card-attribute">
                <span class="card-attribute__value">79</span
                ><span class="card-attribute__name">PHY</span>
              </div>
              <div class="card-attribute" style="margin:auto">
                <span class="card-attribute__value">86</span
                ><span class="card-attribute__name">OVR</span>
              </div>
              
            </div>
            <div class="card-overall" >
                <span class="card-attribute__value"  style="color: #f90; margin:auto">CAM/CM</span
                >
                <!-- <span class="card-attribute__name" ></span> -->
              </div>
          </div>
        </div>

        </div>
      </div>
    </div>
  </div>



</template>

<script>
export default {
  name: "Card-Card",
  props: {
    player: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style scoped>
/* .fifa-card {
  width: 300px;
  background-color: #fff;
  border-radius: 10px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  padding: 16px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.player-info {
  display: flex;
  align-items: center;
  margin-bottom: 16px;
}

.player-image img {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  border: 4px solid #fff;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.player-details {
  margin-left: 16px;
}

.player-name {
  margin: 0;
  font-size: 22px;
  font-weight: bold;
  color: #333;
}

.player-club {
  margin: 4px 0;
  font-size: 14px;
  color: #888;
}

.player-position {
  margin: 0;
  font-size: 14px;
  color: #555;
}

.player-rating {
  background-color: #f2f2f2;
  padding: 8px;
  border-radius: 4px;
  display: inline-block;
  margin-top: 16px;
}

.rating-label {
  margin: 0;
  font-size: 14px;
  color: #888;
}

.rating-value {
  margin: 0;
  font-size: 24px;
  font-weight: bold;
  color: #333;
} */

@import url("https://fonts.googleapis.com/css?family=Roboto:400,400i,700");


.card {
  background: #1c1c4a;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
  color: #7a7ab8;
  display: flex;
}
.card-aside {
  display: flex;
  flex-direction: column;
  text-align: center;
  padding: 10px 0;
  width: 80px;
}
.card-overall {
  margin-bottom: 20px;
}
.card-rating {
  color: #f90;
  display: block;
  font-size: 40px;
  font-weight: bold;
  line-height: 40px;
}
.card-team > img {
  margin: 0 10px;
  margin-bottom: 10px;
  max-height: 50px;
  max-width: 80%;
  width: auto;
}
.card-info {
  font-size: 40px;
  font-weight: bold;
  line-height: 40px;
  margin-top: auto;
}
.card-main {
  flex: 1;
}
.card-header {
  background-image: url("https://static.vecteezy.com/system/resources/previews/000/148/777/non_2x/vector-white-tiger-stripes.png");
  filter: blur(0px);
  background-color: #0f0f3d;
  background-blend-mode: screen;
  display: flex;
  justify-content: center;
  text-align: center;
  position: relative;
}
.card-image {
  width: 80%;
}
.card-name {
  color: #f90;
  border-top: 1px solid;
  border-bottom: 1px solid;
  font-size: 35px;
  font-weight: bold;
  letter-spacing: 3px;
  line-height: 50px;
  margin: 0;
  text-align: center;
}
.card-attribute {
  display: flex;
  flex-direction: row;
  flex-basis: 50%;
  font-size: 30px;
  line-height: 50px;
  text-align: center;
}
.card-attributes {
  background: #0f0f3d;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  padding: 20px 0;
}
.card-attribute__value {
  color: #fff;
  flex-basis: 40%;
  font-size: 35px;
  font-weight: bold;
  margin-right: 6px;
  text-align: right;
}
body {
  background: #eee;
  font-family: "Roboto", sans-serif;
  font-size: 14px;
  font-weight: 400;
  line-height: 20px;
}
.container {
  margin: 50px auto;
  width: 500px;
}
img {
  width: 100%;
  object-fit: cover;
}



</style>
