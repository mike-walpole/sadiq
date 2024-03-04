<script>
	import Youtube from "svelte-youtube-embed";
    
    import { onMount } from 'svelte';
	let shrink = false;

	onMount(() => {
		setTimeout(() => {
			shrink = true;
		}, 600); // Start shrinking 1 second after component mounts
	});

    import jQuery from 'jquery';




	onMount(() => {
		window.jQuery = jQuery;

		var Messenger = function(el){
    'use strict';
    var m = this;
    
    m.init = function(){
      m.codeletters = "&#*+%?£@§$";
      m.message = 0;
      m.current_length = 0;
      m.fadeBuffer = false;
      m.messages = [
        'Travel Industry', 
      ];
      
      setTimeout(m.animateIn, 500);
    };
    
    m.generateRandomString = function(length){
      var random_text = '';
      while(random_text.length < length){
        random_text += m.codeletters.charAt(Math.floor(Math.random()*m.codeletters.length));
      } 
      
      return random_text;
    };
    
    m.animateIn = function(){
      if(m.current_length < m.messages[m.message].length){
        m.current_length = m.current_length + 2;
        if(m.current_length > m.messages[m.message].length) {
          m.current_length = m.messages[m.message].length;
        }
        
        var message = m.generateRandomString(m.current_length);
        jQuery(el).html(message);
        
        setTimeout(m.animateIn, 20);
      } else { 
        setTimeout(m.animateFadeBuffer, 20);
      }
    };
    
    m.animateFadeBuffer = function(){
      if(m.fadeBuffer === false){
        m.fadeBuffer = [];
        for(var i = 0; i < m.messages[m.message].length; i++){
          m.fadeBuffer.push({c: (Math.floor(Math.random()*12))+1, l: m.messages[m.message].charAt(i)});
        }
      }
      
      var do_cycles = false;
      var message = ''; 
      
      for(var i = 0; i < m.fadeBuffer.length; i++){
        var fader = m.fadeBuffer[i];
        if(fader.c > 0){
          do_cycles = true;
          fader.c--;
          message += m.codeletters.charAt(Math.floor(Math.random()*m.codeletters.length));
        } else {
          message += fader.l;
        }
      }
      
      jQuery(el).html(message);
      
      if(do_cycles === true){
        setTimeout(m.animateFadeBuffer, 100);
      } else {
        setTimeout(m.cycleText, 1000);
      }
    };
    
    m.cycleText = function(){
      m.message = m.message + 1;
      if(m.message >= m.messages.length){
        document.getElementById("section-2").scrollIntoView({behavior: "smooth", block: "start", inline: "nearest"});
        m.end();
        
        
      }
      
      m.current_length = 0;
      m.fadeBuffer = false;
      jQuery(el).html('');
      
      setTimeout(m.animateIn, 20);
      
    };
    
    m.init();
  }
  
  console.clear();
  var messenger = new Messenger(jQuery('#messenger'));
  

  
	});

    onMount(() => {
		window.jQuery = jQuery;

		var Messenger2 = function(el){
    'use strict';
    var m = this;
    
    m.init = function(){
      m.codeletters = "&#*+%?£@§$";
      m.message = 0;
      m.current_length = 0;
      m.fadeBuffer = false;
      m.messages = [
        'Thought Leader', 
      ];
      
      setTimeout(m.animateIn, 500);
    };
    
    m.generateRandomString = function(length){
      var random_text = '';
      while(random_text.length < length){
        random_text += m.codeletters.charAt(Math.floor(Math.random()*m.codeletters.length));
      } 
      
      return random_text;
    };
    
    m.animateIn = function(){
      if(m.current_length < m.messages[m.message].length){
        m.current_length = m.current_length + 2;
        if(m.current_length > m.messages[m.message].length) {
          m.current_length = m.messages[m.message].length;
        }
        
        var message = m.generateRandomString(m.current_length);
        jQuery(el).html(message);
        
        setTimeout(m.animateIn, 20);
      } else { 
        setTimeout(m.animateFadeBuffer, 20);
      }
    };
    
    m.animateFadeBuffer = function(){
      if(m.fadeBuffer === false){
        m.fadeBuffer = [];
        for(var i = 0; i < m.messages[m.message].length; i++){
          m.fadeBuffer.push({c: (Math.floor(Math.random()*12))+1, l: m.messages[m.message].charAt(i)});
        }
      }
      
      var do_cycles = false;
      var message = ''; 
      
      for(var i = 0; i < m.fadeBuffer.length; i++){
        var fader = m.fadeBuffer[i];
        if(fader.c > 0){
          do_cycles = true;
          fader.c--;
          message += m.codeletters.charAt(Math.floor(Math.random()*m.codeletters.length));
        } else {
          message += fader.l;
        }
      }
      
      jQuery(el).html(message);
      
      if(do_cycles === true){
        setTimeout(m.animateFadeBuffer, 100);
      } else {
        setTimeout(m.cycleText, 1000);
      }
    };
    
    m.cycleText = function(){
      m.message = m.message + 1;
      if(m.message >= m.messages.length){
        document.getElementById("section-2").scrollIntoView({behavior: "smooth", block: "start", inline: "nearest"});
        m.end();
        
        
      }
      
      m.current_length = 0;
      m.fadeBuffer = false;
      jQuery(el).html('');
      
      setTimeout(m.animateIn, 20);
      
    };
    
    m.init();
  }
  
  console.clear();
  var messenger2 = new Messenger2(jQuery('#messenger2'));
  

  
	});


</script>

<svelte:head>
  <title>Eastern European chain of addiction treatment centers</title>
  <meta charset="UTF-8">
  <meta name="description" content="Sadiq Gillani is a through leader in the Travel Indistry">
  <meta name="keywords" content="drugs, alcohol, addiction, treatment">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
</svelte:head>

<body class="bg-[#1D1C1C] text-white font-Helvetica">
    <div class="flex flex-row px-5 py-5 justify-between items-center sticky top-0 bg-[#1D1C1C] border-b  z-50">
        <img src="/logo.png" alt="logo" class="w-48"> 
        <div class="hidden md:block">
            <a href="/" class="mr-5">Videos</a>
            <a href="/" class="mr-5">Press</a>
            <a href="/" class="mr-5">Coaching</a> 
            <a href="/" class="mr-5">Books</a>
        </div>
        <button class="border border-white rounded-xl px-5 py-3">Get to work ↗</button>
    </div>

    <div class="shrinkable-div flex flex-col justify-end" class:shrink>
        <div class="px-5 pb-10 text-5xl md:text-9xl">
            <h1 id="messenger">?£@§*+$&#%.</h1>
            <h1 id="messenger2">&#*+%?£@§$.</h1>
        </div>
    </div>

<div class="grid md:grid-cols-2 px-5 py-14 border-t">
	<div class="text-4xl md:pr-24 mb-5">Sadiq was born and lives in London and has visited over 120 countries. He is a thought leader on the Travel Industry & Career/Self Development</div>
	<div class="md:columns-2">
		Sadiq is a Senior Advisor for travel at Attestor Capital, where he is Chairman of the Advisory Board for Condor, the second airline of Germany. He sits on the board of eTraveli, an online travel agency owned by CVC Partners, the World Economic Forum's Global Future Council for Travel and is a Trustee of Stonewall. Sadiq is also an Executive Coach founded in the work of Carl Jung. He started an MBA course at Stanford on the Travel & Airline industry and is the subject of a case study in Jeffrey Pfeffer's class "Paths to Power".
</div>
</div>



<div>
    <h1 class="border-t border-b text-3xl px-5 py-8 ">Thought Leadership</h1>
    <div class="grid md:grid-cols-12 border-b">
        <div class="md:col-span-3 md:border-r px-5 pt-10 pb-10">
             <h2 class="text-lg underline mb-2 font-FK">Art of Disciplined Opportunism</h2>
             
             <p class="font-FK">01. Developing a purpose driven career</p>
              <p class="font-FK">02. Understanding power dynamics</p>
               <p class="font-FK">03. Gaining skills to accelerate your career</p>
          
        </div>
        <div class="md:col-span-8 md:border-r pb-10 md:py-10 px-3">
           <div class="md:columns-1 px-3">
            <Youtube id="570XZJpi4dc" />
            
           </div>
        </div>
        <div class="md:col-span-8"></div>
       
    </div>

     <div class="grid md:grid-cols-12 border-b">
        <div class="md:col-span-3 md:border-r px-5 pt-10 pb-10">
             <h2 class="text-lg underline mb-2 font-FK">Body</h2>
           
             <p class="font-FK">01. Tagline 1</p>
              <p class="font-FK">02. Tagline 2</p>
               <p class="font-FK">03. Tagline 3</p>
               
        </div>
        <div class="md:col-span-8 md:border-r pb-10 md:py-10 px-3">
           <div class="md:columns-1 px-3">
            <Youtube id="uXeVJDvJ2-c"/> </div>
        </div>
        <div class="md:col-span-8"></div>
       
    </div>

      
   


</div>
 <h1 class="border-t border-b text-3xl px-5 py-8 ">Press</h1>
<div class="max-w-3xl mx-auto grid md:grid-cols-2 gap-4 mt-10 ">
  <div class="border border-white flex flex-col w-11/12 md:w-full mx-auto">
    <h1 class="text-3xl my-5 mx-auto w-11/12"> Harvard Business School</h1>
    <img src="/press4.webp" loading="lazy" alt="for website" class="w-11/12 mx-auto">
    <a href="https://www.gorman.pl" class="w-11/12 mx-auto text-xl">
      <button class="w-full bg-white text-black hover:bg-black hover:text-white border border-white px-5 py-2 my-3 mx-auto text-xl">Read the article ↗</button>

    </a>
  </div>
  <div class="border border-white mt-0 flex flex-col w-11/12 md:w-full mx-auto">
    <h1 class="text-3xl my-5 mx-auto w-11/12"> World Economic Forum</h1>
    <img src="/press3.webp" loading="lazy" alt="for website" class="w-11/12 mx-auto">
    <button class="w-11/12 bg-white text-black hover:bg-black hover:text-white border border-white px-5 py-2 my-3 mx-auto text-xl">Read the article ↗</button>
  </div>
  <div class="border border-white mt-0 flex flex-col w-11/12 md:w-full mx-auto">
    <h1 class="text-3xl my-5 mx-auto w-11/12"> The Independent</h1>
    <img src="/press2.webp" loading="lazy" alt="for website" class="w-11/12 mx-auto">
    <button class="w-11/12 bg-white text-black hover:bg-black hover:text-white border border-white px-5 py-2 my-3 mx-auto text-xl">Read the article ↗</button>
  </div>
  <div class="border border-white mt-0 flex flex-col w-11/12 md:w-full mx-auto">
    <h1 class="text-3xl my-5 mx-auto w-11/12"> Der Spiegel</h1>
    <img src="/press1.webp" loading="lazy" alt="for website" class="w-11/12 mx-auto">
    <button class="w-11/12 bg-white text-black hover:bg-black hover:text-white border border-white px-5 py-2 my-3 mx-auto text-xl">Read the article ↗</button>
  </div>

</div>





</body>


<style>
	.shrinkable-div {
		width: 100vw;
		height: 70vh;
		background-color: #1D1C1C;
		transition:
			width 2s,
			height 2s;
	}

	.shrink {
		width: 100vw;
		height: 40vh;
	}
</style>
