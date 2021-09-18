<template>
  <div id="test" :class="color">
    <p>Hello World</p>
    <img v-bind:src="imgURL" class="pic" />
    <p>Celcius : {{ celcius }}</p>
    <p>Fahrenheit : {{ fahrenheit }}</p>
    <p>Random : {{ show }}</p>
    <button
      class="btn1"
      variant="info"
      type="button"
      v-on:click="alertMsg('D', 'F', $event)"
    >
      <i class="fas fa-angry"></i>
      Click1
    </button>
    <span />
    <button
      class="btn2"
      variant="dark"
      type="button"
      @click="alertMsg('D', 'F', $event)"
    >
      <i class="far fa-grin-beam-sweat"></i>
      Click2
    </button>
    <span />
    <button class="btn3" variant="success" type="button" @dblclick="logName()">
      <i class="fas fa-sad-cry"></i>
      Click3
    </button>
    <div class="info">
      <div class="card">
        <div class="class-header">
          Name: {{ myInfo.myName }} <span />
          <button
            class="btn4"
            variant="warning"
            type="button"
            @click="myShowInfo()"
          >
            {{ lableButton }}
          </button>
        </div>
        <div class="class-body" v-bind:hidden="!hideShow">
          Nickname: {{ myInfo.myNickname }} ID: {{ myInfo.myStudentID }}
        </div>
      </div>
    </div>
    <div class="container">
      <p>V-model</p>
      <div class="input-group mb-3">
        <span class="input-group-text" id="inputGroup-sizing-default"
          ><i class="fas fa-user"></i
        ></span>
        <input
          type="text"
          class="form-control"
          aria-label="Sizing example input"
          aria-describedby="inputGroup-sizing-default"
          v-model="userName"
        />
      </div>
      <div class="input-group mb-3">
        <span class="input-group-text" id="inputGroup-sizing-default"
          ><i class="fas fa-key"></i
        ></span>
        <input
          type="text"
          class="form-control"
          aria-label="Sizing example input"
          aria-describedby="inputGroup-sizing-default"
          v-model="userPass"
        />
      </div>

      <div class="show">
        Show <br />
        User: {{ userName }} <br />
        Password: {{ userPass }}
      </div>
    </div>
    <div class="container">
      <div class="input-group mb-3">
        <span class="input-group-text" id="inputGroup-sizing-default"
          ><i class="fas fa-palette"></i
        ></span>
        <input
          type="text"
          class="form-control"
          aria-label="Sizing example input"
          aria-describedby="inputGroup-sizing-default"
          v-model="bgColor"
        />
      </div>
      <center>
        <div v-bind:style="{ 'background-color': bgColor }" class="color"></div>
      </center>
    </div>
  </div>
</template>

<script>
export default {
  name: "Test",
  data() {
    return {
      name: "Natchaphon",
      imgName: "French",
      imgURL:
        "https://www.dogthailand.net/data/attachment/forum/201707/12/202212oa1kgg5ae8idadxo.jpg",
      color: "tmp2",
      celcius: 30,
      data: ["หัว", "ก้อย"],
      text: "click",
      myInfo: {
        myName: "Natchaphon Chaloemsong",
        myNickname: "New",
        myStudentID: "6130203136",
      },
      hideShow: true,
      userName: null,
      userPass: null,
      bgColor: null,
    };
  },
  computed: {
    fahrenheit() {
      let result = this.celcius * 1.8 + 32;
      return result;
    },
    random() {
      return Math.random() > 0.5 ? 1 : 0;
    },
    show() {
      return this.data[this.random];
    },
    lableButton() {
      return this.hideShow ? "Hide" : "Show";
    },
  },
  methods: {
    alertMsg(p1, p2, e) {
      alert(`You ${e.type} the button at ${e.clientX}, ${e.clientY}`);
      alert(`parameter ${p1}, ${p2}`);
    },
    logName() {
      console.log("Natchaphon Chaloemsong");
    },
    myShowInfo() {
      this.hideShow = !this.hideShow;
    },
  },
};
</script>

<style>
.tmp {
  background-color: black;
  color: white;
}

.info {
  padding-top: 15px;
  padding-bottom: 15px;
}
.pic {
  border-radius: 50%;
  width: 400px;
  height:400px;
}
.btn1 {
  margin: 10px;
  background-color: royalblue;
  color: aliceblue;
  border: none;
  padding-top: 5px;
  padding-bottom: 5px;
  border-radius: 7px;
}
.btn2 {
  margin: 10px;
  background-color: darkorange;
  color: aliceblue;
  border: none;
  padding-top: 5px;
  padding-bottom: 5px;
  border-radius: 7px;
}
.btn3 {
  margin: 10px;
  background-color: hotpink;
  color: aliceblue;
  border: none;
  padding-top: 5px;
  padding-bottom: 5px;
  border-radius: 7px;
}
.btn4 {
  margin: 10px;
  background-color: lightsalmon;
  color: aliceblue;
  border: none;
  padding-top: 5px;
  padding-bottom: 5px;
  border-radius: 7px;
}
p {
  margin: 10px;
}
.container {
  width: 400px;
}
.color {
  width: 70px;
  height: 70px;
  border-radius: 50%;
}
.show {
  margin: 10px;
}
</style>