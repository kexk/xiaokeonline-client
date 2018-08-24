<template>
    <div>
      

      <div>
        <b-carousel id="carousel1"
                style="text-shadow: 1px 1px 2px #333;"
                controls
                indicators
                background="#ababab"
                :interval="4000"
                img-width="1024"
                img-height="480"
                v-model="slide"
        >

          <!-- Text slides with image -->
          <b-carousel-slide caption="First slide"
                            text="Nulla vitae elit libero, a pharetra augue mollis interdum."
                            img-src="https://picsum.photos/1024/480/?image=52"
          ></b-carousel-slide>

          <!-- Slides with custom text -->
          <b-carousel-slide img-src="https://picsum.photos/1024/480/?image=54">
            <h1>Hello world!</h1>
          </b-carousel-slide>

          <!-- Slides with image only -->
          <b-carousel-slide img-src="https://picsum.photos/1024/480/?image=58">
          </b-carousel-slide>

          <!-- Slides with img slot -->
          <!-- Note the classes .d-block and .img-fluid to prevent browser default image alignment -->
          <b-carousel-slide>
            <img slot="img" class="d-block img-fluid w-100" width="1024" height="480"
                src="https://picsum.photos/1024/480/?image=55" alt="image slot">
          </b-carousel-slide>

          <!-- Slide with blank fluid image to maintain slide aspect ratio -->
          <b-carousel-slide caption="Blank Image" img-blank img-alt="Blank image">
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse
              eros felis, tincidunt a tincidunt eget, convallis vel est. Ut pellentesque
              ut lacus vel interdum.
            </p>
          </b-carousel-slide>

        </b-carousel>

        <section class="body container">
          <b-card-group
                  class="mb-8">
            <b-card title="标题"
                    img-src="https://picsum.photos/600/300/?image=25"
                    img-alt="Image"
                    img-top
                    tag="article"
                    style="width=200px;"
                    class="text-center">
              <p class="card-text">
                这个是说明的文字
              </p>
              <b-button href="#" variant="primary">查看详情</b-button>
            </b-card>

            <b-card title="标题"
                    img-src="https://picsum.photos/600/300/?image=25"
                    img-alt="Image"
                    img-top
                    tag="article"
                    style="width-max: 30rem;"
                    class="text-center">
              <p class="card-text">
                这个是说明的文字
              </p>
              <b-button href="#" variant="primary">查看详情</b-button>
            </b-card>

            <b-card title="Card Title"
                    img-src="https://picsum.photos/600/300/?image=25"
                    img-alt="Image"
                    img-top
                    tag="article"
                    style="max-width: 30rem;"
                    class="text-center">
              <p class="card-text">
                Some quick example text to build on the card title and make up the bulk of the card's content.
              </p>
              <b-button href="#" variant="primary">查看详情</b-button>
            </b-card>
          </b-card-group>

          
            <!-- </b-card> -->
          <!-- </b-card-group> -->
        </section>

        <section id="service">
          <div class="title">
            <h3>服务与支持</h3>
            <span></span>
          </div>

          <div class="body">
            <b-card-group deck>
              <b-card title="Title"
                      img-src="https://picsum.photos/300/300/?image=41"
                      img-alt="Img"
                      class="text-center"
                      
                      img-top>
                  <p class="card-text">
                      This is a wider card with supporting text below as a
                      natural lead-in to additional content. This content
                      is a little bit longer.
                  </p>
                  <div slot="footer">
                      <small class="text-muted">Last updated 3 mins ago</small>
                  </div>
              </b-card>
              <b-card title="Title"
                      img-src="https://picsum.photos/300/300/?image=41"
                      img-alt="Img"
                      img-top>
                  <p class="card-text">
                      This card has supporting text below as a natural lead-in
                      to additional content.
                  </p>
                  <div slot="footer">
                      <small class="text-muted">Last updated 3 mins ago</small>
                  </div>
              </b-card>
              <b-card title="Title"
                      img-src="https://picsum.photos/300/300/?image=41"
                      img-alt="Img"
                      img-top>
                  <p class="card-text">
                      This is a wider card with supporting text below as a natural
                      lead-in to additional content. This card has even longer content
                      than the first to show that equal height action.
                  </p>
                  <div slot="footer">
                      <small class="text-muted">Last updated 3 mins ago</small>
                  </div>
                </b-card>
              </b-card-group>
          </div>

        </section>

        <section id=about>
          <div>
            <b-card overlay
                    img-src="https://picsum.photos/900/250/?image=36"
                    img-alt="关于我们"
                    text-variant="blue"
                    class="text-center"
                    title="关于我们">
              <p class="card-text">
                致力于为中小型企业打造高端的开发部门。
              </p>
              <p class="card-text">
                从此让开发简单
              </p>
            </b-card>
          </div>
        </section>
      </div>

<!-- navbar-1.vue -->
    </div>
</template>

<script>

export default {
  components: {
  }
}
</script>

<style>
.body {
  /* background-color: #ccc; */
  height: 600px;
}

#service {
  /* height: 480px; */
}

#service .title {
  text-align: center
}

.title h3 {
  color: #00b3ff;
}

.title span {
  width: 80px;
  height: 40px;
  border-top: solid 2px #00b3ff;
  display: inline-block;
}

</style>

