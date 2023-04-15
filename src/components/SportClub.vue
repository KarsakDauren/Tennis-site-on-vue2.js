<template>
  <div class="sport-club-wrapper">
    <div class="sport-club-info">
      <h2>Спортивный клуб</h2>

      <p>
        Imperdiet lorem ipsum, pulvinar aliquet sit ultricies in sit turpis.
        Ultricies erat pretium risus quam tincidunt non viverra porttitor.
        Sollicitudin enim nunc in nisi donec vel. Blandit mauris vitae amet
        aliquet ultrices mauris pellentesque. Non ipsum commodo, sit mi sit
        netus aenean nisl. Donec sit pellentesque enim, vestibulum.
        <br /><br />
        Condimentum hac adipiscing purus in augue nisi. Convallis ut nisi.
      </p>
      <div class="sport-list-wrapper">
        <h3>Ornare orci ut dictum nulla fames.</h3>
        <nav>
          <ul>
            <li>
              <p>
                Euismod diam, vel venenatis bibendum sodales sem hendrerit
                vulputate sagittis.
              </p>
            </li>
            <br />
            <li>
              <p>
                Nisl senectus sed malesuada donec. Interdum malesuada bibendum
                imperdiet elementum auctor vitae in.
              </p>
            </li>
            <br />
            <li>
              <p>
                Quam purus ornare dictum pharetra. Sed viverra tellus
                sollicitudin urna, sagittis.
              </p>
            </li>
            <br />
            <li>
              <p>
                Scelerisque urna senectus commodo, nam. Donec nibh tempus
                imperdiet nisi, tincidunt mus egestas nisl nullam.
              </p>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class extends Vue {}
</script>

<style scoped lang="scss">
.sport-club-wrapper {
  position: relative;
  margin-top: 150px;
  &::before {
    content: "";
    display: block;
    width: 526px;
    height: 514px;
    background-image: url("../assets/img/image4.jpg");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    position: absolute;
    z-index: 2;
    margin: 70px 0 70px 110px;
  }
}
.sport-club-info {
  background-color: #f7ece1;
  width: 636px;
  height: 654px;
  padding-top: 70px;
  padding-left: 146px;
  padding-right: 60px;
  padding-bottom: 84px;
  margin-left: 550px;

  .sport-list-wrapper {
    margin-top: 35px;
  }
  h2 {
    font-weight: 400;
    font-size: 36px;
    margin-bottom: 25px;
  }
  p {
    font-size: 14px;
    line-height: 20px;
  }
  h3 {
    margin-top: 35px;
    font-weight: 400;
    font-size: 21px;
  }
  nav {
    margin-top: 25px;
    ul {
      li {
        p {
          font-size: 14px;
          position: relative;
          padding-left: 23px;
          &::before {
            content: "";
            display: block;
            position: absolute;
            width: 8px;
            height: 8px;
            background-color: #8d86c9;
            margin-right: 23px;
            top: 15px;
            left: 0;
          }
        }
      }
    }
  }
}
</style>
