ipaymu Plugins Node .js 
<p></p>
<h1>Example Code </h1> 
<p></p>

import * as ipaymu from "ipaymu";

// ipaymu.setVa("0000008999927923");
// ipaymu.setApiKey("SANDBOX76A13A0D-AD50-4061-9832-F5AF22B541D8-20220316213052");

ipaymu.setVa("1179000899");
ipaymu.setApiKey("QbGcoO0Qds9sQFDmY0MWg1Tq.xtuh1");

let carts = {
    product: ["product 1 ", "product2 "],
    quantity: ["1", "2"],
    price: ["10000", "50000"],
    description: ["product-desc", "product-desc 2"],
    weight: [1, 2],
    height: [10, 10],
    length: [30, 40],
    width: [10, 50],
};

ipaymu.addCart(carts);
ipaymu.setURL({
    ureturn: "https://google.com",
    ucancel: "https://google.com",
    unotify: "https://google.com",
});

let userData = {"name" : "Gusmang Asmara" , "email" : "ibasmara@gmail.com" , "phone" : "081936384166" , "amount" : "40000", "paymentMethod" : "va", "paymentChannel" : "bca"};
ipaymu
    .directPayment(userData)
    .then((res) => console.log(res))
    .catch((err) => console.log(err));