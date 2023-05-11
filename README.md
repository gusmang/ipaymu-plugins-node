ipaymu Plugins Node .js V.1.0.3
<p></p>
<h1>Example Code Direct Payment</h1> 
<p></p>

<div style="padding:20px; background:#EEEEEE;">
import * as ipaymu from "gusmang-ipaymu-node";
<p></p>
ipaymu.setVa("1179000899"); <br />
ipaymu.setApiKey("QbGcoO0Qds9sQFDmY0MWg1Tq.xtuh1");
<p></p>
let carts = { <br />
<div style="padding-left:40px;">
    product: ["product 1 ", "product2 "], <br />
    quantity: ["1", "2"], <br />
    price: ["10000", "50000"], <br />
    description: ["product-desc", "product-desc 2"], <br />
    weight: [1, 2], <br />
    height: [10, 10], <br />
    length: [30, 40], <br />
    width: [10, 50], <br />
</div>
}; 
<p></p>
ipaymu.addCart(carts);<br />
ipaymu.setURL({
<div style="padding-left:40px;">
<br />
    ureturn: "https://google.com",<br />
    ucancel: "https://google.com",<br />
    unotify: "https://google.com",<br />
</div>
});
<p></p>
let userData = {
<div style="padding-left:40px;">    
<br />
"name" : "Gusmang Asmara" , <br />
"email" : "ibasmara@gmail.com" , <br />
"phone" : "081936384166" , <br />
"amount" : "40000", <br />
"paymentMethod" : "va", <br />
"paymentChannel" : "bca"<br />
</div>
};
<p></p>
ipaymu<br />
    .directPayment(userData)<br />
    .then((res) => console.log(res))<br />
    .catch((err) => console.log(err));<br />
</div>

<p></p>
<b> Good Luck & Happy Coding ! </b>