**This example with javascript**



`functionGetPrice(){`

​        `let val = 29` <!--change Quatity Buy-->

​        `const priceOneUnit = 3000` <!-- example for Buy 1-4 Unit-->

​        `const priceSeries = 2000` <!--/example forBuy 5 and multiple 6-->

​        `const priceGrocery = 1000` <!--example for buy 20 and multiple 20-->

​        `let finalPrice = 0`

​        `if(val >= 20){`

​            `let cekGrocery = parseInt(val%20)`

​            `let total = 0;`

​            `if(cekGrocery > 0){`

​                `total = total + ((parseInt(val/20)*20)*priceGrocery)`

​                `let cekSeries = cekGrocery%5`

​                `if(cekSeries > 0){`

​                    `total = total + ((parseInt(cekGrocery/5)*5)*priceSeries) + (cekSeries * priceOneUnit)`                   

​                `}else {`

​                    `total = total + cekGrocery*priceSeries`

​                `}`

​                `finalPrice = total`

​            `}else {`

​                `finalPrice = val * priceGrocery`

​            `}`

​        `}else`

​        `if(val >=5){`

​            `let total = 0;`

​            `let cekSeries = val% 5`

​            `if(cekSeries > 0){`

​                `total = total + ((parseInt(val/5)*5) *priceSeries)`

​                `total = total + cekSeries * priceOneUnit`

​            `}else {`

​                `total = val*priceSeries`

​            `}`

​            `finalPrice = total`

​        `}else`

​        `if(val <5){`

​            `finalPrice = val * priceOneUnit`

​        `}`

​        `return finalPrice`

`}`