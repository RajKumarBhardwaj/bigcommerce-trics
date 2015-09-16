
all varriable call for help

%%Panel.HomeFeaturedProducts%%

#bigcommerce using tabshorizontlly



<h1>Responsive CSS Tabs</h1>

<main>
  
  <input id="tab1" type="radio" name="tabs" checked>
  <label for="tab1">ProductDescription</label>
    
  <input id="tab2" type="radio" name="tabs">
  <label for="tab2">ProductByCategory</label>
    
  <input id="tab3" type="radio" name="tabs">
  <label for="tab3">ProductReviews</label>
    
  <input id="tab4" type="radio" name="tabs">
  <label for="tab4">ProductVideos</label>
    
  <section id="content1">
    <p>
      %%Panel.ProductDescription%%
    </p>
  </section>
    
  <section id="content2">
    <p>
      %%Panel.ProductByCategory%%
    </p>
  </section>
    
  <section id="content3">
    <p>
      %%Panel.ProductReviews%%
    </p>
  </section>
    
  <section id="content4">
    <p>
      %%Panel.ProductVideos%%
    </p>
  </section>
    
</main>

@import url('http://fonts.googleapis.com/css?family=Open+Sans:400,600,700');
@import url('http://netdna.bootstrapcdn.com/font-awesome/4.1.0/css/font-awesome.css');

*, *:before, *:after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html, body {
  height: 100%;
}

body {
  font: 14px/1 'Open Sans', sans-serif;
  color: #555;
  background: #eee;
}

h1 {
  padding: 50px 0;
  font-weight: 400;
  text-align: center;
}

p {
  margin: 0 0 20px;
  line-height: 1.5;
}

main {
  min-width: 320px;
  max-width: 800px;
  padding: 50px;
  margin: 0 auto;
  background: #fff;
}

section {
  display: none;
  padding: 20px 0 0;
  border-top: 1px solid #ddd;
}

input {
  display: none;
}

label {
  display: inline-block;
  margin: 0 0 -1px;
  padding: 15px 25px;
  font-weight: 600;
  text-align: center;
  color: #bbb;
  border: 1px solid transparent;
}

label:before {
  font-family: fontawesome;
  font-weight: normal;
  margin-right: 10px;
}

label[for*='1']:before { content: '\f1cb'; }
label[for*='2']:before { content: '\f17d'; }
label[for*='3']:before { content: '\f16b'; }
label[for*='4']:before { content: '\f1a9'; }

label:hover {
  color: #888;
  cursor: pointer;
}

input:checked + label {
  color: #555;
  border: 1px solid #ddd;
  border-top: 2px solid orange;
  border-bottom: 1px solid #fff;
}

#tab1:checked ~ #content1,
#tab2:checked ~ #content2,
#tab3:checked ~ #content3,
#tab4:checked ~ #content4 {
  display: block;
}

@media screen and (max-width: 650px) {
  label {
    font-size: 0;
  }
  label:before {
    margin: 0;
    font-size: 18px;
  }
}

@media screen and (max-width: 400px) {
  label {
    padding: 15px;
  }
}


