<template>
  <div class="container">
      <div class="card">
        <div class="face face1">
          <div class="content">
            <div class="icon">
              <i class="fab fa-youtube"></i>
            </div>
          </div>
        </div>
        <div class="face face2">
          <div class="content">
            <h3>
              <a
                href="https://www.youtube.com/watch?v=IqLglZLmlu4"
                target="_blank"
                >@WebDevelopment</a
              >
            </h3>
            <p>
              Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ipsam,
              at? Lorem ipsum dolor sit amet consectetur adipisicing elit.
              Laudantium, consectetur!
            </p>
          </div>
        </div>
      </div>
      <div class="card">
        <div class="face face1">
          <div class="content">
            <div class="icon">
              <i class="fab fa-facebook-square"></i>
            </div>
          </div>
        </div>
        <div class="face face2">
          <div class="content">
            <h3>
              <a
                href="https://www.youtube.com/watch?v=IqLglZLmlu4"
                target="_blank"
                >@WebDevelopment</a
              >
            </h3>
            <p>
              Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ipsam,
              at? Lorem ipsum dolor sit amet consectetur adipisicing elit.
              Laudantium, consectetur!
            </p>
          </div>
        </div>
      </div>
      <div class="card">
        <div class="face face1">
          <div class="content">
            <div class="icon">
              <i class="fab fa-twitter"></i>
            </div>
          </div>
        </div>
        <div class="face face2">
          <div class="content">
            <h3>
              <a
                href="https://www.youtube.com/watch?v=IqLglZLmlu4"
                target="_blank"
                >@WebDevelopment</a
              >
            </h3>
            <p>
              Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ipsam,
              at? Lorem ipsum dolor sit amet consectetur adipisicing elit.
              Laudantium, consectetur!
            </p>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  }
}
</script>
<style lang="scss">
body {
  margin: 0;
  padding: 0;
  min-height: 100vh;
  background: #333;
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: sans-serif;
  background-color: #f1f1f1;
}

.container {
  width: 1000px;
  position: relative;
  display: flex;
  justify-content: space-between;
  .card{
    position: relative;
    border-radius: 10px;
    &:nth-child(1){
      .icon{
        background: #ff0000;
      }
    }
    &:nth-child(2){
      .icon{
        background: #4267b2;
      }
    }
    &:nth-child(3){
      .icon{
        background: #00aced;
      }
    }
    .icon{
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      transition: 0.7s;
      z-index: 1;
    }
    .face{
      width: 300px;
      height: 200px;
      transition: 0.5s;
      
    }
    .face1{
      position: relative;
      background: rgb(170, 110, 110);
      display: flex;
      justify-content: center;
      align-items: center;
      z-index: 1;
      transform: translateY(140px);
    }
    .face2{
      position: relative;
      background: #fff;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 20px;
      box-sizing: border-box;
      box-shadow: 0 20px 50px rgba(0, 0, 0, 0.8);
      transform: translateY(-60px);
      .content{
        p{
          margin: 0;
          padding: 0;
          text-align: center;
          color: #414141;
        }
        h3{
          margin: 0 0 10px 0;
          padding: 0;
          color: #fff;
          font-size: 24px;
          text-align: center;
        }
      }
    }
  }
  a{
    text-decoration: none;
    color: #414141;
  }
}


i {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-size: 80px;
  color: #fff;
  transition: 0.7s;
}

.container .card:hover .face.face1 {
  background: #ff0057;
  transform: translateY(0);
  .content{
    opacity: 1;
   transition: 0.5s;
   i{
     max-width: 100px;
   }
  }
}

.container .card:hover .face.face2 {
  transform: translateY(0);
}

</style>
