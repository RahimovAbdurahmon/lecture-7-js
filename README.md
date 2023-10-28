# _LECTURE 7 about Dom_
![](./%D0%91%D0%B5%D0%B7%20%D0%BD%D0%B0%D0%B7%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F%20(2).png)
># _Table of content;_
## _1.Dom_ 
## _2.Bom_
## _3.Events_
## _4.Dom Methods_
># _What is Windows in our brouser?_
## _Window ba 3 kism taqsim meshavad:_
## _1.Dom;_
## _2.bom;_
## _3.Javascript;_
## _Avval bo Js mo kodhoro navista va bad bo dom paivast neskunem va ba bom iane brauser nishon metihem;_
># _What is Dom in Js_
![](./%D0%91%D0%B5%D0%B7%20%D0%BD%D0%B0%D0%B7%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F.jpg)
## _Dom : in Document object model zaboni purrai on meboshad; Dom metavonad html attributhoro ivaz kunad va hamchunin metaavonad style css ro ham ivaz kiunad_
# _-----------------------------------------------_
## _Dom: in Document Object Model ast , ki bo html va Js paivast shuda hodisaro ba amal ovardan art iane hodisai dinamiki io hodisai interacivi; Mo bo document metavonem hamai chizhoiamonro ba brauser nishon btem; vamo html filero  tavasuti tagi script va atributi src paivast mecunem;._
- _Js metavnad hamai elementhoi html-ro ivaz kunad;_
- _Js metavona hamai atributoi html-ro ivaz kunad;_
- _Js metavonad hamai hamai css-hoi html ro ivaz kunad;_ 
- _Js metavonad hamai html element va atributhoro dar harakat_ darorad;_
- _js metavonad iak fili navi html va css sozad_
># _Methos in Dom_
![](./images.jpg)
># _What is quaryselector() method in Dom_
## _quaryselector() baroi giriftani element io tagho az html ba vositai type , class va id_
```
    html:
<h1>Hello</h1> /// only this
<h1>Hello</h1>
<h1>Hello</h1>
<div class="box">HELLO</div>
<button class="btn">click</button>
    Js(Dom):
let a=document.querySelector("h1")
console.log(a);
```
## _quaryseletorAll() elementho ki agar iakchandto iakkhela bo type , id va class_
```
    html:
<h1>Hello</h1> /// this
<h1>Hello</h1> /// this
<h1>Hello</h1> /// this
<div class="box">HELLO</div>
<button class="btn">click</button>
    Js(Dom):
let a=document.querySelector("h1")
console.log(a);
```
## _InnerHTML - injmethod baroi ivaz kardani element io taghoi html ba vositai js_
```
    html:
<h1>Hello</h1>
<div class="box">HELLO</div>
<button class="btn">click</button>
    js:
let a=document.querySelector("h1")
console.log(a);
document.body.innerHTML="Bye"
    output:
Bye;
```
## _How to Style html attributes or elements ; chi khel element hotro style dihem_
```
    html:
<h1>Hello</h1>
<div class="box">HELLO</div>
<button class="btn">click</button>
    js:
let a=document.querySelector("h1")
console.log(a);
a.style.backgroundColor="red";
    output:
hello /// backcol:red
```
## _HTML events (onclick) - baroi rukh dodani iagon hodisa io iagon goro onclick kunem iagon kor dar web-site rukh dihadAn HTML event can be something thebrowser does, or something a user does.Here are some examples of HTML events_
- _An HTML web page has finished loading_
- _An HTML input field was changed_
- _An HTML button was clicked_
```
    html:
<h1>Hello</h1>
<div class="box">HELLO</div>
<button class="btn">click</button>
    js:
    let a=document.querySelector("h1")
let btn2=document.querySelector(".btn")
let div=document.querySelector(".box")
console.log(btn2);
a.innerHTML="Bye"
a.style.backgroundColor = "green"

a.onclick = ()=>{
    btn2.style.backgroundColor = "red"
}
btn2.onclick =() => {
    div.style.backgroundColor="red"
}
    output:
    if click h1 return baccol btn red
    if click btn return backcol box red
```
## _createElement () - baroi sikhtani iagon div io element va tagho_
## _appendChild() baroi ba html paivast kardani element va ba brouser nushon dodan_
```
    html:
<h1>Hello</h1>
<div class="box">HELLO</div>
<button class="btn">click</button>
    js:
let creat=document.createElement("button")
let creat2= document.createElement("p")
creat.innerHTML="hello"
creat2.innerHTML="phragraph"F
document.body.appendChild(creat)
document.body.appendChild(creat2)
    output:
    return one buuton and paragraph;
```
># _Method classlist()_
## _1.add() - baroi dobavot kardani iagon class_
```
    js:
let creat=document.createElement("button")
let creat2= document.createElement("p")
creat.innerHTML="hello"
creat.onclick = () =>{
    creat2.classList.add("par")
}
creat2.innerHTML="phragraph"

document.body.appendChild(creat)
document.body.appendChild(creat2) 
    output:
 agar iak bor buton crat ro(hello) -ro click kunem
 shaklash digar meshavad
```
## _2.remove() - baroi udalit kardani iagoi class_
```
    js:
let creat=document.createElement("button")
let creat2= document.createElement("p")
creat.innerHTML="hello"
creat.onclick = () =>{
    creat2.classList.remove("par")
}
creat2.innerHTML="phragraph"

document.body.appendChild(creat)
document.body.appendChild(creat2) 
    output:
 agar iak bor buton crat ro(hello) -ro click kunem
 udalit meshavd
```
## _3.toggle - baroi iak bor udalit kardan va iak br dabavit karsdan_
```
    js:
let creat=document.createElement("button")
let creat2= document.createElement("p")
creat.innerHTML="hello"
creat.onclick = () =>{
    creat2.classList.toggle("par")
}
creat2.innerHTML="phragraph"

document.body.appendChild(creat)
document.body.appendChild(creat2) 
    output:
 agar iak bor buton crat ro(hello) -ro click kunem
 udalit meshavd
```
># _Events in Dom_
## _Onclick dar vakti zer kardani iagon tugmachai ki mo ba on baroi istifodai iagon logika dodaiem ba amal meoiad_
>## _misol baroi sokhtani iagon modalka va istifodai on ba vositai onclick_
```
for example : html
<dialog class="dialogadd">
        <form class="formadd">
            <input type="text" placeholder="enter your name..." name="name"><br><br>
            <input type="text" placeholder="enter your email..." name="email"><br><br>
            <button type="submit">submit</button>
        </form>
</dialog>

    Javascript:
btnadd.onclick=() => {
    dialogadd.showModal()
    alert(3)
}
``` 
## _Onsubmit in event ba misli onclick kor mekunad ammo dar vakti zer kardai dugmachai enter ham kor mekunad_
>## _misol baroi dobavit kardani iagon odam ba massive objectho_
```
for example : html
<dialog class="dialogadd">
        <form class="formadd">
            <input type="text" placeholder="enter your name..." name="name"><br><br>
            <input type="text" placeholder="enter your email..." name="email"><br><br>
            <button type="submit">submit</button>
        </form>
</dialog>

    Javascript:
btnadd.onclick=() => {
    dialogadd.showModal()
}
formadd.onsubmit=(event) => {
    event.preventDefault()
    let newuser={
        id:data.length + 1,
        name:event.target["name"].value,
        email:formadd["email"].value,
        iscompleted:false
    }
    data.push(newuser)
    get()
    dialogadd.close()
}
```