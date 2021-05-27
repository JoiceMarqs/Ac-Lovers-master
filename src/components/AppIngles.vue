<template>
    <header>
        <nav class="desktop">
            <ul>
                <img src="src\assets\LOGOSITE.png" alt="" class="logo">
                <li class="items items-hover" id="init"><a href="" title="Início">Home </a></li>
                <li class="items items-hover" id="about"><a href="#sobre" title="Sobre">About </a></li>
                <li class="items items-hover" id="prjs"><a href="#paqueras" title="Paqueras">Flirting </a></li>
                <li class="items items-hover" id="cont"><a href="#departamento" title="Departamento">Departments</a></li>
                <li class="items items-hover" id="cont"><a href="#contato" title="Contato ">Contact</a></li>
                <li class="items items-hover" ><a href="/"><q-btn icon="language" /></a></li>
                        <input type="checkbox" id="checkbox-menu" class="btn-input">

            <label for="checkbox-menu" class="btn-label">
            <span></span>
            <span></span>
            <span></span>
            </label>
                <div class="menu-resp">

                    <a href="/" class="menuresp-item" title="Início">Home</a><br>

                    <a href="/sobre" class="menuresp-item" title="Sobre">About</a><br>

                    <a href="/paqueras" class="menuresp-item" title="Paqueras">Flirting</a><br>

                    <a href="/departamento" class="menuresp-item" title="Departamentos">Departments</a><br>

                    <a href="/contato" class="menuresp-item" title="Contato">Contact</a>

                    <a style="color:white;" href=""><q-btn style="color:#aa96da;" icon="language" /></a>
        </div>
            </ul>

        </nav>
        <div class="wrapper-section1">
        <div class="content">
            <div class="blackboard1">
                <p class="text-blackboard" id="texto">The Pantheons's doors are open, just like some student's hearts. Be part of a department, flert, make friends and live good moments with unique people, and for sure, do not touch in someone's food.</p><br>
                <q-btn class="login" to="/login"  type="submit">Login</q-btn>
                    
                <q-btn class="btnjogar2 register-card" to="/registro" type="submit">Registration</q-btn>
            </div>
        </div>
    </div>
    <section class="services " title="Seção sobre o Academic Lovers" id="sobre">
        <p><br><strong class="title ">Academic <span class="logo-rosa ">Lovers</span>? Pantheon University? What is that?
        </strong></p>
        <hr class="border ">
        <div class="cen">
            <div class="service depar">
               <q-icon name="school" style="font-size: 35px; color: #EA2027;margin-bottom: 20px; "></q-icon>
                <p>For better organization, the P.U. manager created a department division and fortunally the scholars who win 100% can choose which one they wanna be part of
                </p>
            </div>
            <div class="service depar">
                <q-icon name="favorite" style="font-size: 35px; color: #EA2027;margin-bottom: 20px; "></q-icon>
                <p>meet diferents personalities with brillant talents, There are 6 (six) diferents options of flirtting that do not care about your gender or orientation. We are free to love.
                </p>
            </div>
            <div class="service depar">
                <q-icon name="face" style="font-size: 30px; color: #EA2027;margin-bottom: 20px; "></q-icon>
                <p>What pronouns would you like flirtatious to use with you? we seek to optimize the best experience for you and we know how important a pronoun is and the weight it carries. Be free, be whoever you want to be! we will support!
                </p>
            </div>
        </div>
    </section>
    <section class="services " title="Paqueras" id="paqueras">
  <p><strong class="title "> Flirting</strong></p>
  <hr class="border ">
  <div class="q-pa-md">
    <div class="q-gutter-md">
      <q-carousel
        v-model="slide"
        transition-prev="jump-right"
        transition-next="jump-left"
        swipeable
        animated
        control-color="white"
        navigation
        padding
        arrows
        height="300px"
        class="shadow-1 rounded-borders" style="background:#aa96da;"
      >
        <q-carousel-slide name="style" class="column no-wrap flex-center">
          <div class="q-mt-md text-center">
            <q-img
                src="src\assets\apollo-head.png" style="width: 100px; height: 100px;" contain></q-img>
            {{ lorem }}
          </div>
        </q-carousel-slide>

        <q-carousel-slide name="layers" class="column no-wrap flex-center">
          <div class="q-mt-md text-center">
            <q-img
                src="src\assets\naomi-head.png" style="width: 100px; height: 100px;" contain></q-img>
            {{ lorem2 }}
          </div>
        </q-carousel-slide>
        <q-carousel-slide name="map" class="column no-wrap flex-center">
          <div class="q-mt-md text-center">
            <q-img
                src="src\assets\kae-head.png" style="width: 100px; height: 100px;" contain></q-img>
            {{ lorem3 }}
          </div>
        </q-carousel-slide>
      </q-carousel>
    </div>
  </div>
  <br>
  </section>
  <section class="services " title="Seção sobre os Departamentos da Universidade Pantheon " id="departamento">
        <p><strong class="title ">Departments</strong></p>
        <hr class="border ">
        <p>Oh! haven't you chosen one yet? Well, let's show you a little bit about them hehe… 
        </p>

        <div class="cen">
            <div class="service depar">
                <q-icon name="functions" style="font-size: 30px; color: #192a56;margin-bottom: 10px;"></q-icon>
                <h2>Exact Sciences</h2>
                <p>Complicated theorems, fascinating theories and incredible logic for everything! Ideal for those looking for a love like numbers, growing and infinite! Here the feelings are constant and not variable. 
                </p>
            </div>
            <div class="service depar">
                <q-icon name="biotech" style="font-size: 30px; color: #44bd32; margin-bottom: 10px; "></q-icon>
                <h2>Biological and Medical Sciences</h2>
                <p>Behind incredible experiments and serious faces there is an explosive action that includes desire and confidence. The formula of love is capable of deconcentrating even the best of scientists. Find your unique way of living.
                </p>
            </div>
            <div class="service depar">
                <q-icon name="history_edu" style="font-size: 30px; color: #e1b12c; margin-bottom: 10px; "></q-icon>
                <h2>Human Sciences</h2>
                <p>The language of feelings is like a work of art, or writing, complex and admired. Perfect for those who always seek to express themselves using their imagination and creativity within themselves in the best way.. 
                </p>
            </div>
            <div class="service depar">
                <q-icon name="developer_board" style="font-size: 30px; color: #2c3e50; margin-bottom: 10px; "></q-icon>
                <h2>Information technology (T.I)</h2>
                <p>The incredible world of T.I, complex, logical and creative! Ideal for those who love coffee and dark circles, technology and its features! In T.I it is unacceptable to serve weak emotions and coffee! 
                </p>
            </div>
        </div>
    </section>
    <section class="services " title="Contato " id="contato">
        <p><br><strong class="title"> Contact</strong></p>
        <hr class="border ">
        <p> <strong>Wait! still not following us on social media ?! How will you find out about the news this way? Follow it and don't regret it!</strong></p>

        <div class="social-media ">
            <a href="#" style="text-decoration:none;"><q-icon name="facebook" style="font-size: 50px; color: #0066CC; "></q-icon></a>
            <a href="#" style="text-decoration:none;"><q-icon name="gmail" style="font-size: 50px; color: #EA2027;"></q-icon></a>
        </div>
    </section>
    <footer>
            <img src="src\assets\LOGOSITE.png" alt="" class="logo1">
        <ul class="list-footer ">
            <li><a href="/ " title="Início ">Home</a></li>
            <li><a href="/login " title="Login ">Legal mentions</a></li>
            <li><a href="/login " title="Login ">Cookies</a></li>
            <li><a href="/login " title="Login ">Videos Policy</a></li>
        </ul>
        <div class="social-media ">
            <a href="https://www.instagram.com/fatectq/?hl=pt-br "><i class="fab fa-instagram " style="font-size: x-large; color: #4b4b4b; "></i></a>
            <a href="https://twitter.com/FatecTQ "><i class="fab fa-twitter " style="font-size: x-large; color: #4b4b4b; "></i></a>
            <a href="https://www.youtube.com/ "><i class="fab fa-youtube " style="font-size: x-large; color: #4b4b4b; "></i></a>
        </div>

        <p class="copyrights ">&copy; 2021 Queendom - Otome Games.</p>
        <a class="gotopbtn" href="#"> <q-icon name="expand_less"></q-icon></a>
    </footer>
    </header>
    
</template>
