<template>
  <section class="section tile is-ancestor notification is-dark" style="margin: 0 auto; border-radius: 0;">
    <div class="tile is-parent is-vertical">
      <article class="tile is-child box">
        <h2 class="title is-1 has-text-centered has-text-black">Quick Overview</h2>
        <p>Hi! My name is Wesley Ford.  I am a student currently studying computer science at PCC. I really enjoy programming and I am always working on new projects. </p>
      </article>
      <article class="tile is-ancestor has-background-black">
        <div class="tile is-parent is-vertical">
          <h2 class="title is-2 has-text-centered" style="margin-left: 20px;">My Projects</h2>
          <div class="tile is-child media" style="margin-left: 15px;">
            <b-tooltip label="Advance stock analyzer" position="is-right">
              <figure class="image media-left is-4by2" style="max-width: 115px;">
                <a href="https://github.com/Sergix/analyst">
                  <img class="is-rounded" src="https://raw.githubusercontent.com/Sergix/analyst/master/.github/logo-padded.png" style="margin-bottom: 5px;"/>
                </a>
              </figure>
            </b-tooltip>
            <div class="media-content">
              <p><b>[ Disclaimer still under development ]</b><br> This stock analyzer was made to help users trade on the stock market. To help us accomplish this goal we use an advanced back-end server that determines several different factors and predictions from machine models and other great APIs. My area of expertise in this project was mostly the backend flask server. My friend Sergix was in charge of the front-end. He used the nuxtjs framework and buefy to quickly make the front end. You can find <a href="sergix.net">sergix</a> here or on <a href="https://github.com/Sergix">github</a>. </p><br>
              <b-button v-on:click="button_to_redirect('https://github.com/Sergix/analyst-server')">Server repository</b-button> 
            </div>
          </div>
          <div class="tile is-child media" style="margin-left: 15px;">
            <b-tooltip label="Outreach website for a podcast" position="is-right">
              <figure class="image media-left" >
                <h2 class="title is-4" style="color: rgb(186, 85, 211);">Mango Morning</h2>
              </figure>
            </b-tooltip>
            <div class="media-content">
              <p>I made a website for the mango morning podcast. I used gridsome, Cloudflare worker and the SendGrid API</p><br>
              <b-button v-on:click="button_to_redirect('https://github.com/ntohq/mango-morning--website')">Website repository</b-button> 
            </div>
          </div>
          <div class="tile is-child media" style="margin-left: 15px;">
            <b-tooltip label="A website for developers" position="is-right">
              <figure class="image media-left is-4by2" style="max-width: 115px;">
                <a href="https://ntohq.dev">
                  <img class="is-rounded" src="../assets/logoName.png" style="margin-bottom: 5px; background-color: #19FF11;"/>
                </a>
              </figure>
            </b-tooltip>
            <div class="media-content">
              <i>ntohq for developers</i><br style="margin-bottom: 15px;">
              <b>[ Disclaimer still under development ]</b>
              <p>Ntohq is a web app for developers. I used for this project gridsome, mongoDB, github API, and Buefy.</p>
              <i>ntohq.dev is still under development. Some features will not be available at this time.</i><br style="margin-bottom: 20px;">
              <b-button v-on:click="button_to_redirect('https://github.com/ntohq/ntohq-dev/')">Website repository</b-button> 
            </div>
          </div>
        </div>
        <div class="tile is-parent is-vertical has-text-centered box notification is-primary">
          <h2 class="title is-2">My skills</h2>
          <p>Here is a list of the skills I have acquired</p>
          <div class="tile is-parent">
            <div class="tile is-child is-vertical has-text-left">
              <h2 class="title is-3" style="margin-bottom: 0;">Front end</h2>
              <ul style="margin-left: 10px; margin-bottom: 10px;">
                <li>css</li>
                <li>js</li>
                <li>html</li>
              </ul>
            </div>
          </div>
          <div class="tile is-parent">
            <div class="tile is-child is-vertical has-text-left">
              <h2 class="title is-3" style="margin-bottom: 0;">Back-end</h2>
              <ul style="margin-left: 10px; margin-bottom: 10px;">
                <li>
                  <p>Python</p>
                  <ul style="margin-left: 10px;">
                    <li>Flask</li>
                  </ul>
                </li>
                <li>
                  <p>C++</p>
                </li>
                <li>C#</li>
              </ul>
            </div>
          </div>
          <div class="tile is-parent">
            <div class="tile is-child is-vertical has-text-left">
              <h2 class="title is-3" style="margin-bottom: 0;">Frameworks</h2>
              <ul style="margin-left: 10px; margin-bottom: 10px;">
                <li>Vuejs</li>
                <li>Gridsome</li>
                <li>Bulma and buefy</li>
              </ul>
            </div>
          </div>
          <div class="tile is-parent">
            <div class="tile is-child is-vertical has-text-left">
              <h2 class="title is-3" style="margin-bottom: 0;">Miscellaneous</h2>
              <ul style="margin-left: 10px; margin-bottom: 10px;">
                <li>Cloudflare Workers</li>
                <li>SQL</li>
                <li>Arduino</li>
                <li>Soldering</li>
                <li>
                  <p>DIY Projects</p>
                  <ul style="margin-left: 10px; margin-bottom: 10px;">
                    <li>Soldering station</li>
                  </ul>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </article>
    </div>
  </section>  
</template>

<script>
export default {
  methods: {
    button_to_redirect:function(to_link){
      window.location.href = to_link;
    }
  }
}
</script>

<style>
  ul {
    list-style: decimal;
  }

  li {
    font-weight: bold;
  }

  ul li ul li {
    list-style: circle;
    font-style: italic;
  }
</style>