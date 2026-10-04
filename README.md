<!DOCTYPE html>
<!-- saved from url=(0059)file:///C:/Users/lenovo/Downloads/Prorate%20Calculator.html -->
<html lang="en"><head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Prorate Calculator</title>
<style>
:root{--bg:#f4f5f7;--card:#fff;--ink:#1c2430;--mut:#6b7686;--line:#e1e5ea;--acc:#1b6ec2;--ok:#157a43;--bad:#c53030;--sum:#eaf3fc;
box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#12161c;--card:#1b212a;--ink:#e8ecf1;--mut:#97a2b1;--line:#2c3541;--acc:#5aa6ee;--ok:#4cc27f;--bad:#f07b7b;--sum:#18283a}}
:root[data-theme="dark"]{--bg:#12161c;--card:#1b212a;--ink:#e8ecf1;--mut:#97a2b1;--line:#2c3541;--acc:#5aa6ee;--ok:#4cc27f;--bad:#f07b7b;--sum:#18283a}
html{scroll-padding-top:env(safe-area-inset-top,0px)}
body{margin:0;background:var(--bg);color:var(--ink);font-family:system-ui,-apple-system,"Segoe UI",Arial,sans-serif;padding:20px}
.box{max-width:920px;margin:auto;background:var(--card);border:1px solid var(--line);border-radius:12px;padding:22px}
h1{font-size:22px;margin:0 0 4px}
.sub{color:var(--mut);margin:0 0 18px;font-size:14px}
.set{display:grid;grid-template-columns:repeat(auto-fit,minmax(170px,1fr));gap:14px;margin-bottom:16px}
label{display:block;font-size:13px;font-weight:600;margin-bottom:5px}
input,select{width:100%;box-sizing:border-box;padding:9px 10px;border:1px solid var(--line);border-radius:6px;font:inherit;background:var(--bg);color:var(--ink)}
input:focus,select:focus,button:focus-visible{outline:2px solid var(--acc);outline-offset:1px}
.wrap{overflow-x:auto}
table{width:100%;border-collapse:collapse;min-width:640px}
th,td{padding:8px;border-bottom:1px solid var(--line);text-align:right;font-variant-numeric:tabular-nums}
th:first-child,td:first-child{text-align:left}
th{font-size:13px;color:var(--mut);font-weight:600}
td input{padding:7px 8px}
td:first-child input{min-width:110px}
td:nth-child(2) input{min-width:100px;text-align:right}
tfoot td{font-weight:700;border-bottom:0}
button{font:inherit;border:0;border-radius:6px;padding:9px 14px;cursor:pointer;color:#fff;background:var(--acc)}
button.x{background:transparent;color:var(--bad);padding:6px 8px}
.bar{display:flex;gap:10px;margin-top:14px;flex-wrap:wrap}
.sum{margin-top:18px;padding:16px;background:var(--sum);border-left:4px solid var(--acc);border-radius:6px}
.sum p{margin:4px 0;display:flex;justify-content:space-between}
.sum .t{font-size:20px;font-weight:700;margin-top:8px}
.note{font-size:13px;color:var(--mut);margin-top:10px}
.err{color:var(--bad);font-size:13px;min-height:18px;margin-top:8px}
:root{--g:#12874a;--gbg:#e3f6ec;--o:#c2610c;--obg:#fdeedd;--b:#1b6ec2;--bbg:#e2eefb;--p:#6a3fc4;--pbg:#ece6fb;--hd:#1b6ec2;--hd2:#6a3fc4}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){--g:#4cc27f;--gbg:#14301f;--o:#f0a45f;--obg:#3a2713;--b:#6db3f5;--bbg:#142a40;--p:#b79bf5;--pbg:#271d45;--hd:#164a82;--hd2:#47298a}}
:root[data-theme="dark"]{--g:#4cc27f;--gbg:#14301f;--o:#f0a45f;--obg:#3a2713;--b:#6db3f5;--bbg:#142a40;--p:#b79bf5;--pbg:#271d45;--hd:#164a82;--hd2:#47298a}
.box{padding:0;overflow:hidden}
.hero{background:linear-gradient(120deg,var(--hd),var(--hd2));color:#fff;padding:22px}
.hero h1{margin:0 0 4px}.hero .sub{color:#e8eaff;margin:0}
.in{padding:20px 22px 22px}
.step{display:flex;align-items:center;gap:10px;font-weight:700;margin:18px 0 10px;font-size:16px}
.step:first-child{margin-top:0}
.step i{font-style:normal;width:26px;height:26px;border-radius:50%;background:var(--b);color:#fff;display:grid;place-items:center;font-size:14px}
.set>div{background:var(--bbg);padding:12px;border-radius:8px}
thead th{background:var(--bbg);color:var(--b)}
th:nth-child(4),td:nth-child(4){color:var(--g);background:var(--gbg)}
th:nth-child(6),td:nth-child(6){color:var(--o);background:var(--obg)}
th:nth-child(7),td:nth-child(7){color:var(--b);background:var(--bbg);font-weight:700}
tfoot td{background:var(--pbg);color:var(--p)}
.explain{margin-top:14px;padding:12px 14px;background:var(--pbg);color:var(--ink);border-radius:8px;font-size:14px;line-height:1.5;border-left:4px solid var(--p)}
.cards{display:grid;grid-template-columns:repeat(auto-fit,minmax(140px,1fr));gap:10px}
.card{border-radius:10px;padding:12px 14px}
.card span{display:block;font-size:13px;margin-bottom:4px}
.card strong{font-size:20px;font-variant-numeric:tabular-nums}
.c1{background:var(--bbg);color:var(--b)}.c2{background:var(--gbg);color:var(--g)}.c3{background:var(--pbg);color:var(--p)}.c4{background:var(--obg);color:var(--o)}
.final{margin-top:12px;background:linear-gradient(120deg,var(--hd),var(--hd2));color:#fff;border-radius:10px;padding:16px 18px;display:flex;justify-content:space-between;align-items:center;font-size:18px}
.final b{font-size:28px;font-variant-numeric:tabular-nums}
.note{padding:0 22px 20px;margin:0}
</style>
</head>
<body>
<div class="box">
<div class="hero"><h1>Prorate calculator</h1>
<p class="sub">Split one discount fairly across your items, then add tax.</p></div>
<div class="in">
<div class="step"><i>1</i>Enter the discount and tax</div>
<div class="set">
  <div><label for="mode">Discount type</label>
    <select id="mode"><option value="amount">Total discount amount (prorated)</option><option value="percent">Discount % on each item</option></select></div>
  <div><label for="disc" id="discLabel">Total discount amount</label><input id="disc" type="number" min="0" step="any" value="500"></div>
  <div><label for="tax">Tax %</label><input id="tax" type="number" min="0" step="any" value="16"></div>
</div>

<div class="step"><i>2</i>List your items</div>
<div class="wrap">
<table>
<thead><tr><th>Item</th><th>Price</th><th>% of total</th><th>Discount (−)</th><th>Price after discount</th><th>Tax (+)</th><th>You pay</th><th></th></tr></thead>
<tbody id="rows"><tr><td><input type="text" value="Item 1"></td><td><input type="number" class="amt" min="0" step="any" value="2619.61"></td><td class="sh">68.6%</td><td class="d">342.92</td><td class="ad">2276.69</td><td class="tx">364.27</td><td class="fi">2640.96</td><td><button class="x" aria-label="Remove item">✕</button></td></tr><tr><td><input type="text" value="Item 2"></td><td><input type="number" class="amt" min="0" step="any" value="1200"></td><td class="sh">31.4%</td><td class="d">157.08</td><td class="ad">1042.92</td><td class="tx">166.87</td><td class="fi">1209.79</td><td><button class="x" aria-label="Remove item">✕</button></td></tr></tbody>
<tfoot><tr><td>Total</td><td id="tA">3819.61</td><td id="tS">100%</td><td id="tD">500.00</td><td id="tAD">3319.61</td><td id="tT">531.14</td><td id="tF">3850.75</td><td></td></tr></tfoot>
</table>
</div>
<div class="err" id="err"></div>
<div class="bar"><button id="add">+ Add item</button></div>

<div class="explain" id="explain"><b>How it works:</b> the 500.00 discount is shared by price. <b>Item 1</b> is 68.6% of the total (2619.61 of 3819.61), so it takes 68.6% of the discount = <b>342.92</b>. Then 16% tax is added to what is left.</div>

<div class="step"><i>3</i>See the result</div>
<div class="cards">
  <div class="card c1"><span>Original total</span><strong id="sO">3819.61</strong></div>
  <div class="card c2"><span>Total discount</span><strong id="sD">500.00</strong></div>
  <div class="card c3"><span>After discount</span><strong id="sAD">3319.61</strong></div>
  <div class="card c4"><span>Total tax</span><strong id="sT">531.14</strong></div>
</div>
<div class="final"><span>Final total to pay</span><b id="sF">3850.75</b></div>
</div>
<p class="note">Rounded to cents. Any leftover cent goes to the item with the biggest remainder, so the parts always add up exactly.</p>
</div>

<script>
var rowsEl=document.getElementById("rows"),n=0;
var f=function(c){return (c/100).toFixed(2)};
var toC=function(v){return Math.round((parseFloat(v)||0)*100)};

function addRow(name,amt){
  n++;
  var tr=document.createElement("tr");
  tr.innerHTML='<td><input type="text" value="'+(name||"Item "+n)+'"></td>'+
    '<td><input type="number" class="amt" min="0" step="any" value="'+(amt==null?"":amt)+'"></td>'+
    '<td class="sh">0%</td><td class="d">0.00</td><td class="ad">0.00</td><td class="tx">0.00</td><td class="fi">0.00</td>'+
    '<td><button class="x" aria-label="Remove item">&#10005;</button></td>';
  rowsEl.appendChild(tr);
}

function calc(){
  var mode=document.getElementById("mode").value;
  var dv=parseFloat(document.getElementById("disc").value)||0;
  var tr=parseFloat(document.getElementById("tax").value)||0;
  var rows=[].slice.call(rowsEl.children);
  var a=rows.map(function(r){return toC(r.querySelector(".amt").value)});
  var S=a.reduce(function(x,y){return x+y},0);
  var d=a.map(function(){return 0}), err="";

  if(mode==="percent"){
    d=a.map(function(x){return Math.round(x*dv/100)});
  }else{
    var D=Math.round(dv*100);
    if(D>S&&S>0){D=S;err="Discount is larger than the total, so it was capped at "+f(S)+".";}
    if(S>0){
      var base=a.map(function(x){return Math.floor(D*x/S)});
      var left=D-base.reduce(function(x,y){return x+y},0);
      var order=a.map(function(x,i){return {i:i,r:(D*x)%S}}).sort(function(p,q){return q.r-p.r});
      for(var k=0;k<left;k++)base[order[k].i]++;
      d=base;
    }
  }
  var tot={a:0,d:0,ad:0,t:0,f:0};
  rows.forEach(function(r,i){
    var ad=a[i]-d[i], t=Math.round(ad*tr/100), fin=ad+t;
    r.querySelector(".sh").textContent=S?(a[i]/S*100).toFixed(1)+"%":"0%";
    r.querySelector(".d").textContent=f(d[i]);
    r.querySelector(".ad").textContent=f(ad);
    r.querySelector(".tx").textContent=f(t);
    r.querySelector(".fi").textContent=f(fin);
    tot.a+=a[i];tot.d+=d[i];tot.ad+=ad;tot.t+=t;tot.f+=fin;
  });
  var set=function(id,v){document.getElementById(id).textContent=f(v)};
  set("tA",tot.a);set("tD",tot.d);set("tAD",tot.ad);set("tT",tot.t);set("tF",tot.f);
  set("sO",tot.a);set("sD",tot.d);set("sAD",tot.ad);set("sT",tot.t);set("sF",tot.f);
  document.getElementById("tS").textContent=S?"100%":"0%";
  document.getElementById("err").textContent=err;
  var ex="",i0=a.findIndex(function(x){return x>0});
  if(mode==="percent"){
    ex="<b>How it works:</b> every item gets "+dv+"% off its price. Then "+tr+"% tax is added to the discounted price.";
  }else if(i0>=0){
    var nm=rows[i0].querySelector("input").value||"Item";
    ex="<b>How it works:</b> the "+f(Math.min(Math.round(dv*100),S))+" discount is shared by price. <b>"+nm+"</b> is "+(a[i0]/S*100).toFixed(1)+"% of the total ("+f(a[i0])+" of "+f(S)+"), so it takes "+(a[i0]/S*100).toFixed(1)+"% of the discount = <b>"+f(d[i0])+"</b>. Then "+tr+"% tax is added to what is left.";
  }else ex="Enter a price for at least one item to see how the discount is shared.";
  document.getElementById("explain").innerHTML=ex;
}

document.getElementById("mode").addEventListener("change",function(){
  var p=this.value==="percent";
  document.getElementById("discLabel").textContent=p?"Discount %":"Total discount amount";
  document.getElementById("disc").value=p?10:500;
  calc();
});
document.getElementById("add").addEventListener("click",function(){addRow("",0);calc();});
rowsEl.addEventListener("click",function(e){
  if(e.target.classList.contains("x")){e.target.closest("tr").remove();calc();}
});
document.addEventListener("input",calc);

addRow("Item 1",2619.61);addRow("Item 2",1200);addRow("Item 3",850.5);
calc();
</script>


</body></html>
