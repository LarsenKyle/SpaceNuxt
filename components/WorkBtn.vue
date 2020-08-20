<template>
  <div class="discover">
    <div class="icons">
      <a target="_blank" href="https://github.com/LarsenKyle/">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="68.236"
          height="73.086"
          viewBox="0 0 68.236 73.086"
        >
          <path
            id="Icon_feather-github"
            data-name="Icon feather-github"
            d="M26.3,61.473C9.658,66.466,9.658,53.15,3,51.485M49.607,71.46V58.576a11.219,11.219,0,0,0-3.129-8.689c10.453-1.165,21.439-5.127,21.439-23.3A18.108,18.108,0,0,0,62.926,14.1a16.878,16.878,0,0,0-.3-12.553S58.7.384,49.607,6.476a44.543,44.543,0,0,0-23.3,0C17.215.384,13.287,1.549,13.287,1.549a16.878,16.878,0,0,0-.3,12.551A18.11,18.11,0,0,0,7.994,26.684c0,18.044,10.986,22.005,21.439,23.3A11.219,11.219,0,0,0,26.3,58.576V71.46"
            transform="translate(-1.181 0.126)"
            fill="none"
            stroke="#a64de9"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="3"
          />
        </svg>
      </a>
      <a target="_blank" href="https://www.linkedin.com/in/kyle-larsen-046a2b147/">
        <svg xmlns="http://www.w3.org/2000/svg" width="77.737" height="74" viewBox="0 0 77.737 74">
          <g
            id="Icon_feather-linkedin"
            data-name="Icon feather-linkedin"
            transform="translate(-1.5 -1.5)"
          >
            <path
              id="Path_91"
              data-name="Path 91"
              d="M36.626,12A21.626,21.626,0,0,1,58.252,33.626v25.23H43.835V33.626a7.209,7.209,0,0,0-14.417,0v25.23H15V33.626A21.626,21.626,0,0,1,36.626,12Z"
              transform="translate(19.485 15.143)"
              fill="none"
              stroke="#a64de9"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="3"
            />
            <path
              id="Path_92"
              data-name="Path 92"
              d="M3,13.5H17.417V56.752H3Z"
              transform="translate(0 17.248)"
              fill="none"
              stroke="#a64de9"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="3"
            />
            <path
              id="Path_93"
              data-name="Path 93"
              d="M17.417,10.209A7.209,7.209,0,1,1,10.209,3,7.209,7.209,0,0,1,17.417,10.209Z"
              fill="none"
              stroke="#a64de9"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="3"
            />
          </g>
        </svg>
      </a>
    </div>
    <v-btn @click="myWork" depressed height="55px" color="#a64de9" class="btn">Discover My Work</v-btn>
  </div>
</template>

<script>
export default {
  methods:{
    myWork(){
      this.$router.push({path: "work"})
    }
  }
}
</script>

<style lang="scss">
.discover {
  position: absolute;
  top: 50vh;
  left: 12vw;
}
.bg-img {
  .btn {
    color: white;
    width: 300px;
    font-size: 1.2rem;
    letter-spacing: 1.5px;
  }
}
@media only screen and (max-width: 1500px) {
  .bg-img{
    .btn{
      width: 200px;
      font-size: 1rem;
    
    }
  }
}
</style>