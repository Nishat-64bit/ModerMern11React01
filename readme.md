------------------------------------------------------------------    
                know about React Introduction Very Important <Start>
    -------------------------------------------------------------------
    //catch them

    // const count = document.querySelector(".count")
    // const btn = document.querySelector(".btn")
    // let x = 0
    // btn.addEventListener("click",function(){
    //     x = x+1;
    //     count.innerHTML = x ; 
    // })
    // bar bar reload hobe 
    // protibar click page noton kore re paint korse 
    // so aebabe jokon bar bar repaint korse ba dom e interactivity bar bar reload hocce tokon page ta bari
    // hobe ba slow hoe jabe 


    // moloto ekane dom slow na // jodi apnake kibe html css jekono kicu paint ta boli 

    // html ==> htmlparser ==> dom 
    // css ==> cssparser ==> cssom


    // dom + cssom ==>  // rendertree ==> layout ==> painting //
    // aekane jotobar user click korbe totobar e dom update hobe ==> rendertree ==> layout ==> painting
    // aebabe ekta website e jodi onekgulo interactiviy thake tokon 
    // eksate onek user jokon site interactivity korbe site slow hoe jabe // 
    // aekane dom kintu slow korce na, korce dom theke jokono seta barbar rendertree ==> layout ==> painting //
    // abr dom update rendertree ==> layout ==> painting // 
    // aebabe site hoe jabe slow 

    // ? As a result React Comes /// and se kibabe ae proble solve kore 

    // react jeta kore seta holo 
    // 1st e se real dom er ekta copy manne virtual dom create kore 
    // then jototoko update hoice ba change hoise sudo seitoko part er render tree paint korai 
    // bass jeta update hoi nai seitake se repaint kore na 
    // ! react kibabe boze je aekane change hoise ?
    // react reconcililation algorithm use kore 
    // google theke 
    /**
    * Reconciliation is React's way of diffing the virtual DOM tree with the updated virtual DOM to determine the most efficient way to update the real DOM. This process allows React to apply only the necessary changes to the DOM, avoiding the costly operation of updating the entire DOM tree
    */


    // react jeta kore seta holo 
    // 1st e se real dom er ekta copy manne virtual dom create kore 
    // then jokon kono change ba interactivity hobe tokon se virtual dom e update kore dibe 
    // then se react diffing/ reconcillation algorithm maaddome se real dom and virtual dom ae 2tar modde compare korbe 
    // jokon se dekbe tar virtual dom e update hoise kicu jaigai kintu real dom e oijaiga gulo te update hoi nai tokon sei 
    // sudu oi partgulo te real dom e update kore dibe // kintu sob part korbe na karon sob part e tow change hoi nai virtual dom
    // aete kore barbar rendering process kome jabe
    // tai bola jai react ektu fast // not fastest 

    // ? react er ki sobida ase ?? 
    // simply apne dom ami cacci 3ta button jeta te click kore mann 3ta btn er e value barbe ,
    // ekon ekta jinis keal koren aek e kaj korte kintu amr logic lekte hocce 3ta , so 
    // react jeta kore se ekta component make kore rakbe tjemon nicer logic tar moto , then amr jotobar lagbe 
    // oigulate se barbar change korte parve ,, amke bar bar logic likte hocce na aar
    // react e bar bar logic create korte hocce na 

    // ---------------------------------------------ek e kaj kintu logic likte hocce 3bar 
    // const count = document.querySelector(".count")
    // const btn = document.querySelector(".btn")
    // const count1 = document.querySelector(".count1")
    // const btn1 = document.querySelector(".btn1")
    // const count2 = document.querySelector(".count2")
    // const  btn2= document.querySelector(".btn2")

    // let x = 0
    // btn.addEventListener("click",function(){
    //     x = x+1;
    //     count.innerHTML = x ; 
    // })

    // let y = 0
    // btn1.addEventListener("click",function(){
    //     y = y+1;
    //     count1.innerHTML = y ; 
    // })

    // let z = 0
    // btn2.addEventListener("click",function(){
    //     z = z+1;
    //     count2.innerHTML = z ; 
    // })

    /// ------------------------------------------------------------------------
    //=============================================================================================================
    // ? EKON ASEN React code e kaj kore kemne ?? 

    // doren amra ekta normal dom create korsi ..

    // const body = document.body
    // const div = document.createElement("div")
    // const p = document.createElement("p")
    // const span = document.createElement("span")
    // span.innerHTML = "Hello Nishat"
    // p.appendChild(span)
    // div.appendChild(p) // append child holo function
    // body.appendChild(div)
    // console.log(body);

    // react kaj kore 
    // 1st e se ekta blank html markup nei jekane 1ta root id naam div ase .. , jei root e se render korbe 

    /**
    * <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
    </head>
    <body>
    //!  <div id ="root"></div> 
        <script src="intro.js"></script>
    </body>
    </html>
    */

    // then se aei root er maje jebabe dom kaj korsilo serroko kaj korbe 
    // const root = document.querySelector("#root")
    // const div = document.createElement("div")
    // const p = document.createElement("p")
    // const span = document.createElement("span")
    // span.innerHTML = "Hello Nishat"
    // p.appendChild(span)
    // div.appendChild(p) // append child holo function
    // root.append(div)
    // console.log(body);


    //=============================================================================================================

    // kintu amra react e ase erokom kaj dom er moto korbo na , react er niger ekta way ase .. 
    // tai react ke add korte hobe 2ta react and react dom cdn link add koren 
    // console.log(React); calie deken 


    //----------------------------------------------
    // const root = document.querySelector("#root")
    // const div = document.createElement("div")
    // const p = document.createElement("p")
    // const span = document.createElement("span")
    // span.innerHTML = "Hello Nishat"
    // p.appendChild(span)
    // div.appendChild(p) // append child holo function
    // root.append(div)
    // console.log(body);
    //----------------------------------------------

    // react uporrer dom ke niger way te banai //

    const MyComponent = React.createElement("div",null,"Hello World") // ? null bolte ae component er maje bahir theke kicu add korte chacci na , tai ami null raksi , jodi add kortam taile aeta change hoto

    //=============================================================================================================


    // ekon ami uporer dom er moto div er bitore ekta p cie , p er vitor span cie kibabe kobo ?
    const MyComponent = React.createElement("div",null,React.createElement("p",null,React.createElement("span",null,"this is span")))


    ReactDOM.createRoot(document.querySelector("#root")).render(MyComponent)
    ReactDOM.createRoot(document.querySelector("#root")).render(MyComponent) // aekane root ta holo body 

    console.log(MyComponent);

    //=============================================================================================================
    // aekon aei puro jinis mane componet je make korlam ta jodi funtion return kora jeto taile better hoto ?
    const MyComponent = React.createElement("div",null,React.createElement("p",null,React.createElement("span",null,"this is span")))

    function hello1(){
        return(MyComponent)
    }
    ReactDOM.createRoot(document.querySelector("#root")).render(hello1()) // hello1() dilei kaj korbe , naile se tor bozbe na aeta je function 
    //=============================================================================================================

    // ! aekon jodi upore my component ke ami function er maje  korate pari and logic o likte pari taile function e best jekono component er ketre 
    // ? and ami cie upore mycomponet er bitore jebbae code kora ta na kore function er bitore as usual html code likte cacci , tahole seta amder jonno bettor hoto, kintu seta possible na , tobe 1ta way ase , amra jodi amder html code ke babel (react compiler) run korai tokon se se html ke react dom e conver kore 

    // html code  kore then ==>

    <div>
    <p><span>this is span</span></p>
    </div> 

    // babbel ==> html ==> react code >> aeta ke varibale nea ==> root er maje render kolei bass oke 

    /*#__PURE__*/React.createElement("div", null, /*#__PURE__*/React.createElement("p", null, /*#__PURE__*/React.createElement("span", null, "this is span"))); // pure means : 1ta input dile output obiously pawwa jabe 
    //=============================================================================================================

    // kintu amr div to aerokom multiple thakte pare sei ketre babel kaj kore na multiple element er ketre ?
    // solve : just multiple element mane 2/3/etc div ke main ekta div e nen bass oke . se complie kore dibe ae file e thaka obstai apnar react code lika lagbe na , jodi babe cdn thake 
    // multiple html element :

    // aeta amr kaj 
    <div>
    <div>
        <p><span>this is span</span></p>
    </div> 

    <div>
        <p><span>this is span</span></p>
    </div>
    </div> 

    // babel ==> react // aaeta babel er kaj se amr html ke convert kore nibe js and browser ke bozabe

    const component = /*#__PURE__*/React.createElement("div", null, /*#__PURE__*/React.createElement("div", null, /*#__PURE__*/React.createElement("p", null, /*#__PURE__*/React.createElement("span", null, "this is span"))), /*#__PURE__*/React.createElement("div", null, /*#__PURE__*/React.createElement("p", null, /*#__PURE__*/React.createElement("span", null, "this is span"))));

    function hello1(){
        return(component)
    }

    ReactDOM.createRoot(document.querySelector("#root")).render(hello1()) 
    // output : this is span
            //  this is span
    //=============================================================================================================
    // ? tahole kaj ta kemne hoi babel er ??

    const mycomponet = (
    <div>
        <p><span>this is Nishat</span></p>
    </div> 
    );

    function hello(){
        return mycomponet
    }
    ReactDOM.createRoot(document.querySelector("#root")).render(hello())
    // babel ekon kaj korse na // tabe aeta oder problem amder na // 
    //===============================================================================================

    // tobe amra ciele my component aar alada na reke function e nea aste pari 

    // Ex-1 
    function hello(){
        return(
            <div>
                <p><span>this is Nishat</span></p>
            </div> 
            );
    }
    ReactDOM.createRoot(document.querySelector("#root")).render(hello())

    // Ex-2
    // component 1: hello 1
    function hello1(){
        // function body // logical layer 
        const nishat = ()=>{
            console.log("hello");
        }
        // function body  // logical layer 

        return(
            // jsx // javascript xml 
            <div>
                <p>Hello Nishat, <span onClick={nishat}>I think</span> You are a Software Engineer </p>
            </div>
            // jsx //
        )
    }
    // component : hello 1

    // component 2: getdata()
    function getdata(){
        const btn = ()=>{
            console.log("Downloaded");
        }
        return(
            <div>
                <h2>This is Nishat</h2>
                <button onClick={btn}>Downnload Info</button>
            </div>
        )
    }
    // component 2: getdata()
    ReactDOM.createRoot(document.querySelector("#root")).render(getdata())


    // aekon amra tow aerokom babe use korbo na aerokom cdn link setup korlam , 
    /// ekta webpack nite hobe seta holo vite : next class 
    ------------------------------------------------------------------    
               know about React Introduction <End>
    -------------------------------------------------------------------