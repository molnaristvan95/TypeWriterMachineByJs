<!DOCTYPE html>
<html oncontextmenu="return false">
<head>
<meta name="description" content="Írógép">
  <meta charset="MSZ_7795.3">
  <meta name="viewport" content="width=device-width">
  <title>Írógép</title>
  <style>
 *{
  margin:0;
 }
 h1{
  word-wrap: break-word;
  line-heigh:.9;
  displa:inline;
  font-siz:4vw;
  width:90%;
  margin-left:5%;
  text-align:justify;
  text-shadow:1px 1px 3px #f007;
  letter-spacing:.25px;
  word-spacing:1px;
}
p{
  height:1.5rem;
  font-size:1.3rem;
  padding:0;
  margin:0;
  color:red;
}
button{
  width:90%;
  margin-left:5vw;
  height:10vh;
  margin-top:3vh;
}
a{
  pointer-events:none;
  opacity:0;
}
body{
  user-select:none;
}
  </style>
  <script>
  function writing(){
  txt = 'ez egy string amely hosszú lesz egyszer, vagy annál is hosszabb ha olyanra írod =D <br> A három medve <br>Egyszer egy leányka elment hazulról az erdőre. Eltévedt az erdőn, s keresni kezdte az utat hazafelé. Nem találta, de egyszer csak elérkezett egy házikóhoz.Az ajtó nyitva volt, benéz az ajtón, látja, hogy senki sincs a házikóban, s bemegy.Három medve lakott ebben a házikóban. Egyik volt az apa, Mihail Ivanics, nagy volt és borzas. Másik volt az anya. Ez kisebb volt. Nasztaszja Petrovna volt a neve. Kis medvebocs volt a harmadik, úgy hívták: Misutka.A mackók nem voltak otthon, elmentek sétálni az erdőre.Két szobája volt a házikónak. A leányka bement az első szobába, s három tányért látott az asztalon, leves volt bennük. Az első tányér nagy volt, Mihail Ivanics tányérja, a másik, a kisebb, Nasztaszja Petrovnáé, a harmadik, kis kék tányérka, a Misutkáé. Mindegyik tányér mellett kanál is volt: egy nagy, egy közepes, meg egy kicsi.A leányka kezébe vette a nagy kanalat, kanalazott vele a nagy tányérból, azután fogta a közepes kanalat, kanalazott vele a közepesből, azután fogta a kis kanalat, kanalazott vele a kicsi kék tányérból. Misutka levese esett a legjobban neki.A leányka szeretett volna leülni, s három széket látott az asztal körül: egy nagyot, a Mihail Ivanicsét, egy kisebbet, a Nasztaszja Petrovnáét, s egy harmadikat, egészen kicsit, kék párnácskával, a Misutkáét.Felmászott a nagy székre, de leesett róla; azután ráült a középső székre, de kényelmetlen volt neki, azután ráült a kicsi székre és elnevette magát - olyan jólesett az ülés rajta.Térdére vette a kék kistányért és enni kezdett. Megette mind a levest és elkezdett a széken himbálódzni.A kis szék eltört, s a leányka leesett a földre. Felkelt, felemelte a kis széket s bement a másik szobába. Ott három ágyat látott; az egyik nagy volt: Mihail Ivanics ágya, a másik közepes: Nasztaszja Petrovnáé, a harmadik - Misutkáé.A leányka belefeküdt a nagy ágyba - túlságosan tágas volt neki; belefeküdt a közepesbe - túlságosan magas volt neki; belefeküdt a kis ágyba - beleillett, mintha neki szabták volna, s el is aludt benne.Hazajöttek a medvék nagy éhesen; s hozzá akartak látni az ebédhez.A nagy medve vette a tányérját, belenézett, s elbődült rettenetes hangon: - Ki evett az én tányéromból?Nasztaszja Petrovna megnézte a tányérját, s elordította magát, ha nem is olyan dörgő hangon: - Ki evett az én tányéromból?Misutka pedig meglátta az üres tányért, s így sipítozott cérnahangon: - Ki evett az én tányéromból, és ki ette meg egy cseppig a levesemet?Mihail Ivanics ránézett a székére, s elordította magát rettenetes hangon: - Ki ülhetett a székemen, s ki mozdíthatta el a helyéről?Nasztaszja Petrovna ránézett a székére, s elordította magát, ha nem is olyan dörgő hangon: - Ki ülhetett a székemen, s ki mozdíthatta el a helyéről?Misutka ránézett az eltört kicsi székre, s ezt sipította: - Ki ülhetett a székemen, s ki törhette el a lábát?Aztán bementek a másik szobába.- Ki feküdt az ágyamon, s ki gyűrte össze? - bőgte Mihail Ivanics rettenetes hangon.- Ki feküdt az ágyamon, s ki gyűrte össze? - bőgte Nasztaszja Petrovna, ha nem is olyan dörgő hangon.Misutka pedig odatolta a kicsi széket az ágyhoz, felmászott az ágyába, s ezt sipította cérna-hangon:- Ki feküdt bele az ágyamba?S egyszerre meglátta a leánykát s olyat visított, mintha a húsába hasítottak volna.- Itt van! Fogják meg! Fogják meg! Ajajaj! Fogják meg!És meg akarta harapni a kislányt.A leányka kinyitotta szemét, megpillantotta a medvéket s az ablakhoz rohant.Nyitva volt az ablak, a leányka kiugrott rajta és elmenekült. A medvék pedig nem érték utol.';
  len = txt.length;
  tomb =[];
  lenTime = -1;
  function timing(){
    if(tomb.length<=len){
      setTimeout(function() { timing() ; },10);
      tomb.push(txt.charAt(lenTime));
      newStr = tomb.join('');
    document.getElementById('txt2').innerHTML=newStr;
      lenTime++;
    }
  }
  timing();
}
writing();


function re(){
  if(lenTime!=len){
    tomb = [];
    newStr = '';
    writing();
  }
  else if(lenTime==len){
    writing();
  }
}

function fontSizeByScreenWidthOrHeight(){
  var sw = screen.width;
  var sh = screen.height;
  var body = document.getElementsByTagName('BODY')[0];
  if(sw>sh){
    //body.style.fontSize='calc((1vh + 1vw) * .8)';
    body.style.fontSize='2vh';
    body.style.background='#00f1';
  }
  else if(sw<sh){
    //body.style.fontSize='calc((1vh + 1vw) * .8)';
    body.style.fontSize='2vw';
    body.style.background='#f001';
  }
  setTimeout(function() { fontSizeByScreenWidthOrHeight() ; },10);
}
fontSizeByScreenWidthOrHeight();
  </script>
</head>
<body>
<h1 style="color:#faa;" id="txt">Írógép<br>LOL</h1>
  <h1 onclick="background='red'" id="txt2">Here come the txt<br>A javascript jelenleg nem fut. <br>ez valószínűleg egy egyszerű HTML megjelenítő. <br>Kérlek másold be az oldal linkjét Chrome-ba!<hr>https://output.jsbin.com/mefacut</h1>
  <button onclick="re()" type="button">Restart</button>
</body>
</html>

