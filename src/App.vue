<template>
  <div id="app">
    <carousel-section></carousel-section>
    <div class="row mb-3 ml-auto mr-auto">
      <div class="col-xs-6 col-sm-10 col-md-8 col-lg-7 mg">
        <div class="card">
          <div class="mr-1 mt-1 ml-1 mb-2">
            <img class="card-img-top" src="./assets/img/Sea.jpg" alt />
          </div>
          <div class="card-body">
            <counter @p1="sum" />
          </div>
        </div>
      </div>
      <div class="col-xs-6 col-sm-2 col-md-4 col-lg-5 bg">
        
        <div class="tot"><i class="fas fa-angle-double-right"></i>
        Total {{total}} point.</div>
      </div>
      <!--/col-md-6 total-->
    </div>

    <div class="row mb-3 ml-auto mr-auto">
      <div class="col-xs-6 col-sm-10 col-md-8 col-lg-7 mg">
        <div class="card">
          <div class="mr-1 mt-1 ml-1 mb-2">
            <img class="card-img-top" src="./assets/img/mountain.jpg" alt />
          </div>
          <div class="card-body">
            <counter @p2="sum1" />
          </div>
        </div>
      </div>
      <div class="col-xs-6 col-sm-2 col-md-4 col-lg-5 bg">
        <div class="tot"><i class="fas fa-angle-double-right"></i>
        Total {{tl}} point.</div>
      </div>
      <!--/col-md-6 total-->
    </div>

    <div class="row mb-3 ml-auto">
      <div class="col-xs-6 col-sm-10 col-md-8 col-lg-7 mg">
        <div class="card">
          <div class="mr-1 mt-1 ml-1 mb-2">
            <img class="card-img-top" src="./assets/img/Island.jpg" />
          </div>
          <div class="card-body">
            <counter @p3="sum2" />
          </div>
        </div>
      </div>
      <div class="col-xs-6 col-sm-2 col-md-4 col-lg-5 bg">
        <div class="tot"><i class="fas fa-angle-double-right"></i>
        Total {{t}} point. </div>
      </div>
      <!--/col-md-6 total-->
    </div>

    <footer>
      Copyright &copy;
      All rights reserved | This
      template is made with
      <i
        class="fa fa-heart-o"
        aria-hidden="true"
      ></i> by
      <a href="#" target="_blank">Nalin</a>

      <br />
      <div class="te">
        <b>CONTACT</b>
        <div>
          <a href="https://web.facebook.com/SNalinN/" target="blank">
            <i class="fab fa-facebook text-dark fa-2x mr-2"></i>
          </a>
          <a href="http://line.me/ti/p/~nnasoma" target="blank">
            <i class="fab fa-line fa-2x text-dark mr-2"></i>
          </a>
          <a href="https://www.instagram.com/iiinaliniii/" target="blank">
            <i class="fab fa-instagram-square fa-2x text-dark mr-2"></i>
          </a>
          <a href="https://mail.google.com/mail/u/0/?tab=rm&ogbl#inbox" target="blank">
            <i class="far fa-envelope text-dark fa-2x mr-2"></i>
          </a>
          <a href="https://github.com/Nalin2000/likelove6.git" target="blank">
            <i class="fab fa-github text-dark fa-2x mr-2"></i>
          </a>
        </div>
      </div>
    </footer>
  </div>
</template>




<script>
import carouselSection from "./components/CarouselSection";
import counter from "./components/counter";
export default {
  name: "App",
  components: {
    counter,
    carouselSection,
  },

  data: function () {
    return {
      total: 0, //ผลรวมทั้งหมด
      tl: 0,
      t: 0,
    };
  },
  methods: {
    sum(counterValue) {
      this.total += counterValue;
    },
    sum1(countValue) {
      this.tl += countValue;
    },
    sum2(cValue) {
      this.t += cValue;
    },
  },
};
</script>

<style scope>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #000000;
}
.bg {
  font-size: 3rem;
  display: flex;
  justify-content: center;
  align-items: center;

}
.mg {
  display: flex;
  justify-content: center;
  align-items: center;
}
.card {
  width: 27rem;
  margin-top: 60px;
}

footer {
  background: rgba(255, 255, 255, 0.384);
  padding: 20px;
}
p {
  color: rgb(0, 0, 0);
  text-align: center;
}
.te {
  text-align: left;
  margin-top: 20px;
}
.tot {
  background-color: rgba(238,238,238,0.6);
  padding: 20px;
  border-radius: 20px;
}
</style>
