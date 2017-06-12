# EKC-classification


import tensorflow as tf
import math
import numpy as np


IRIS_TEST2 = "A07002.csv"

IRIS_TEST4 = "A07004.csv"

IRIS_TEST7 = "A07007.csv"
IRIS_TEST8 = "A07008.csv"
IRIS_TEST9 = "A07009.csv"
IRIS_TEST10 = "A07010.csv"
IRIS_TEST11 = "A07011.csv"
IRIS_TEST12 = "A07012.csv"

IRIS_TEST15 = "A07015.csv"
IRIS_TEST16 = "A07016.csv"

IRIS_TEST19 = "A07019.csv"
IRIS_TEST20 = "A07020.csv"
IRIS_TEST21 = "A07021.csv"
IRIS_TEST22 = "A07022.csv"
IRIS_TEST23 = "A07023.csv"
IRIS_TEST24 = "A07024.csv"
IRIS_TEST25 = "A07025.csv"
IRIS_TEST26 = "A07026.csv"

IRIS_TEST28 = "A07028.csv"


IRIS_TEST32 = "A07032.csv"
IRIS_TEST33 = "A07033.csv"
IRIS_TEST34 = "A07034.csv"
IRIS_TEST35 = "A07035.csv"
IRIS_TEST36 = "A07036.csv"
IRIS_TEST37 = "A07037.csv"

IRIS_TEST39 = "A07039.csv"
IRIS_TEST40 = "A07040.csv"
IRIS_TEST41 = "A07041.csv"
IRIS_TEST42 = "A07042.csv"
IRIS_TEST43 = "A07043.csv"
IRIS_TEST44 = "A07044.csv"
IRIS_TEST45 = "A07045.csv"

IRIS_TEST47 = "A07047.csv"
IRIS_TEST48 = "A07048.csv"

IRIS_TEST50 = "A07050.csv"
IRIS_TEST51 = "A07051.csv"
IRIS_TEST52 = "A07052.csv"
IRIS_TEST53 = "A07053.csv"
IRIS_TEST54 = "A07054.csv"
IRIS_TEST55 = "A07055.csv"
IRIS_TEST56 = "A07056.csv"
IRIS_TEST57 = "A07057.csv"
IRIS_TEST58 = "A07058.csv"
IRIS_TEST59 = "A07059.csv"
IRIS_TEST60 = "A07060.csv"

IRIS_TEST63 = "A07063.csv"

IRIS_TEST65 = "A07065.csv"

IRIS_TEST70 = "A07070.csv"

IRIS_TEST73 = "A07073.csv"
IRIS_TEST74 = "A07074.csv"
IRIS_TEST75 = "A07075.csv"

IRIS_TEST77 = "A07077.csv"
IRIS_TEST78 = "A07078.csv"
IRIS_TEST79 = "A07079.csv"
IRIS_TEST80 = "A07080.csv"
IRIS_TEST81 = "A07081.csv"
IRIS_TEST82 = "A07082.csv"

IRIS_TEST85 = "A07085.csv"
IRIS_TEST86 = "A07086.csv"

IRIS_TEST88 = "A07088.csv"
IRIS_TEST89 = "A07089.csv"
IRIS_TEST90 = "A07090.csv"

IRIS_TEST92 = "A07092.csv"

IRIS_TEST94 = "A07094.csv"
IRIS_TEST95 = "A07095.csv"
IRIS_TEST96 = "A07096.csv"
IRIS_TEST97 = "A07097.csv"
IRIS_TEST98 = "A07098.csv"

IRIS_TEST100 = "A07100.csv"
IRIS_TEST101 = "A07101.csv"
IRIS_TEST102 = "A07102.csv"
IRIS_TEST103 = "A07103.csv"
IRIS_TEST104 = "A07104.csv"
IRIS_TEST105 = "A07105.csv"
IRIS_TEST106 = "A07106.csv"
IRIS_TEST107 = "A07107.csv"
IRIS_TEST108 = "A07108.csv"
IRIS_TEST109 = "A07109.csv"
IRIS_TEST110 = "A07110.csv"
IRIS_TEST111 = "A07111.csv"
IRIS_TEST112 = "A07112.csv"
IRIS_TEST113 = "A07113.csv"
IRIS_TEST114 = "A07114.csv"
IRIS_TEST115 = "A07115.csv"
IRIS_TEST116 = "A07116.csv"
IRIS_TEST117 = "A07117.csv"
IRIS_TEST118 = "A07118.csv"

IRIS_TEST120 = "A07120.csv"
IRIS_TEST121 = "A07121.csv"
IRIS_TEST122 = "A07122.csv"
IRIS_TEST123 = "A07123.csv"
IRIS_TEST124 = "A07124.csv"
IRIS_TEST125 = "A07125.csv"
IRIS_TEST126 = "A07126.csv"
IRIS_TEST127 = "A07127.csv"
IRIS_TEST128 = "A07128.csv"
IRIS_TEST129 = "A07129.csv"
IRIS_TEST130 = "A07130.csv"
IRIS_TEST131 = "A07131.csv"


IRIS_TEST134 = "A07134.csv"

IRIS_TEST140 = "A07140.csv"
IRIS_TEST141 = "A07141.csv"
IRIS_TEST142 = "A07142.csv"
IRIS_TEST143 = "A07143.csv"

IRIS_TEST146 = "A07146.csv"
IRIS_TEST147 = "A07147.csv"

IRIS_TEST149 = "A07149.csv"

IRIS_TEST151 = "A07151.csv"
IRIS_TEST152 = "A07152.csv"
IRIS_TEST153 = "A07153.csv"


IRIS_TEST158 = "A07158.csv"

IRIS_TEST160 = "A07160.csv"
IRIS_TEST161 = "A07161.csv"

IRIS_TEST163 = "A07163.csv"
IRIS_TEST164 = "A07164.csv"
IRIS_TEST165 = "A07165.csv"

IRIS_TEST167 = "A07167.csv"
IRIS_TEST168 = "A07168.csv"
IRIS_TEST169 = "A07169.csv"
IRIS_TEST170 = "A07170.csv"

IRIS_TEST173 = "A07173.csv"
IRIS_TEST174 = "A07174.csv"
IRIS_TEST175 = "A07175.csv"
IRIS_TEST176 = "A07176.csv"

IRIS_TEST178 = "A07178.csv"

IRIS_TEST180 = "A07180.csv"
IRIS_TEST181 = "A07181.csv"
IRIS_TEST182 = "A07182.csv"
IRIS_TEST183 = "A07183.csv"
IRIS_TEST184 = "A07184.csv"

IRIS_TEST186 = "A07186.csv"

IRIS_TEST188 = "A07188.csv"
IRIS_TEST189 = "A07189.csv"
IRIS_TEST190 = "A07190.csv"
IRIS_TEST191 = "A07191.csv"
IRIS_TEST192 = "A07192.csv"
IRIS_TEST193 = "A07193.csv"

IRIS_TEST196 = "A07196.csv"
IRIS_TEST197 = "A07197.csv"
IRIS_TEST198 = "A07198.csv"
IRIS_TEST199 = "A07199.csv"
IRIS_TEST200 = "A07200.csv"
IRIS_TEST201 = "A07201.csv"

IRIS_TEST204 = "A07204.csv"
IRIS_TEST205 = "A07205.csv"
IRIS_TEST206 = "A07206.csv"
IRIS_TEST207 = "A07207.csv"

IRIS_TEST209 = "A07209.csv"
IRIS_TEST210 = "A07210.csv"
IRIS_TEST211 = "A07211.csv"
IRIS_TEST212 = "A07212.csv"

IRIS_TEST216 = "A07216.csv"

IRIS_TEST218 = "A07218.csv"

IRIS_TEST220 = "A07220.csv"
IRIS_TEST221 = "A07221.csv"
IRIS_TEST222 = "A07222.csv"
IRIS_TEST223 = "A07223.csv"
IRIS_TEST224 = "A07224.csv"
IRIS_TEST225 = "A07225.csv"

IRIS_TEST227 = "A07227.csv"
IRIS_TEST228 = "A07228.csv"

IRIS_TEST230 = "A07230.csv"
IRIS_TEST231 = "A07231.csv"
IRIS_TEST232 = "A07232.csv"

IRIS_TEST234 = "A07234.csv"
IRIS_TEST235 = "A07235.csv"
IRIS_TEST236 = "A07236.csv"

IRIS_TEST238 = "A07238.csv"
IRIS_TEST239 = "A07239.csv"

IRIS_TEST241 = "A07241.csv"
IRIS_TEST242 = "A07242.csv"
IRIS_TEST243 = "A07243.csv"
IRIS_TEST244 = "A07244.csv"

IRIS_TEST246 = "A07246.csv"

IRIS_TEST248 = "A07248.csv"

IRIS_TEST250 = "A07250.csv"


IRIS_TEST253 = "A07253.csv"

IRIS_TEST255 = "A07255.csv"
IRIS_TEST256 = "A07256.csv"
IRIS_TEST257 = "A07257.csv"
IRIS_TEST258 = "A07258.csv"
IRIS_TEST259 = "A07259.csv"
IRIS_TEST260 = "A07260.csv"

IRIS_TEST262 = "A07262.csv"

IRIS_TEST264 = "A07264.csv"

IRIS_TEST266 = "A07266.csv"
IRIS_TEST267 = "A07267.csv"
IRIS_TEST268 = "A07268.csv"
IRIS_TEST269 = "A07269.csv"
IRIS_TEST270 = "A07270.csv"

IRIS_TEST272 = "A07272.csv"
IRIS_TEST273 = "A07273.csv"

IRIS_TEST275 = "A07275.csv"
IRIS_TEST276 = "A07276.csv"

IRIS_TEST278 = "A07278.csv"
IRIS_TEST279 = "A07279.csv"

IRIS_TEST281 = "A07281.csv"
IRIS_TEST282 = "A07282.csv"

IRIS_TEST284 = "A07284.csv"
IRIS_TEST285 = "A07285.csv"

IRIS_TEST287 = "A07287.csv"
IRIS_TEST288 = "A07288.csv"

IRIS_TEST291 = "A07291.csv"

IRIS_TEST293 = "A07293.csv"
IRIS_TEST294 = "A07294.csv"
IRIS_TEST295 = "A07295.csv"
IRIS_TEST296 = "A07296.csv"

IRIS_TEST298 = "A07298.csv"
IRIS_TEST299 = "A07299.csv"
IRIS_TEST300 = "A07300.csv"
IRIS_TEST301 = "A07301.csv"

IRIS_TEST303 = "A07303.csv"
IRIS_TEST304 = "A07304.csv"
IRIS_TEST305 = "A07305.csv"

IRIS_TEST307 = "A07307.csv"

IRIS_TEST309 = "A07309.csv"
IRIS_TEST310 = "A07310.csv"
IRIS_TEST311 = "A07311.csv"
IRIS_TEST312 = "A07312.csv"
IRIS_TEST313 = "A07313.csv"

IRIS_TEST315 = "A07315.csv"

IRIS_TEST317 = "A07317.csv"
IRIS_TEST318 = "A07318.csv"
IRIS_TEST319 = "A07319.csv"


IRIS_TEST323 = "A07323.csv"
IRIS_TEST324 = "A07324.csv"
IRIS_TEST325 = "A07325.csv"
IRIS_TEST326 = "A07326.csv"
IRIS_TEST327 = "A07327.csv"

IRIS_TEST330 = "A07330.csv"
IRIS_TEST331 = "A07331.csv"
IRIS_TEST332 = "A07332.csv"
IRIS_TEST333 = "A07333.csv"
IRIS_TEST334 = "A07334.csv"
IRIS_TEST335 = "A07335.csv"
IRIS_TEST336 = "A07336.csv"
IRIS_TEST337 = "A07337.csv"

IRIS_TEST339 = "A07339.csv"
IRIS_TEST340 = "A07340.csv"
IRIS_TEST341 = "A07341.csv"

IRIS_TEST343 = "A07343.csv"
IRIS_TEST344 = "A07344.csv"
IRIS_TEST345 = "A07345.csv"
IRIS_TEST346 = "A07346.csv"
IRIS_TEST347 = "A07347.csv"

IRIS_TEST349 = "A07349.csv"

IRIS_TEST351 = "A07351.csv"
IRIS_TEST352 = "A07352.csv"
IRIS_TEST353 = "A07353.csv"
IRIS_TEST354 = "A07354.csv"

IRIS_TEST356 = "A07356.csv"
IRIS_TEST357 = "A07357.csv"

IRIS_TEST359 = "A07359.csv"
IRIS_TEST360 = "A07360.csv"
IRIS_TEST361 = "A07361.csv"
IRIS_TEST362 = "A07362.csv"

IRIS_TEST364 = "A07364.csv"
IRIS_TEST365 = "A07365.csv"
IRIS_TEST366 = "A07366.csv"

IRIS_TEST368 = "A07368.csv"
IRIS_TEST369 = "A07369.csv"
IRIS_TEST370 = "A07370.csv"
IRIS_TEST371 = "A07371.csv"
IRIS_TEST372 = "A07372.csv"
IRIS_TEST373 = "A07373.csv"
IRIS_TEST374 = "A07374.csv"
IRIS_TEST375 = "A07375.csv"
IRIS_TEST376 = "A07376.csv"
IRIS_TEST377 = "A07377.csv"
IRIS_TEST378 = "A07378.csv"
IRIS_TEST379 = "A07379.csv"
IRIS_TEST380 = "A07380.csv"
IRIS_TEST381 = "A07381.csv"

IRIS_TEST383 = "A07383.csv"
IRIS_TEST384 = "A07384.csv"
IRIS_TEST385 = "A07385.csv"
IRIS_TEST386 = "A07386.csv"

IRIS_TEST389 = "A07389.csv"
IRIS_TEST390 = "A07390.csv"
IRIS_TEST391 = "A07391.csv"
IRIS_TEST392 = "A07392.csv"
IRIS_TEST393 = "A07393.csv"
IRIS_TEST394 = "A07394.csv"

IRIS_TEST396 = "A07396.csv"
IRIS_TEST397 = "A07397.csv"
IRIS_TEST398 = "A07398.csv"
IRIS_TEST399 = "A07399.csv"
IRIS_TEST400 = "A07400.csv"
IRIS_TEST401 = "A07401.csv"
IRIS_TEST402 = "A07402.csv"
IRIS_TEST403 = "A07403.csv"
IRIS_TEST404 = "A07404.csv"

IRIS_TEST406 = "A07406.csv"
IRIS_TEST407 = "A07407.csv"


IRIS_TEST410 = "A07410.csv"
IRIS_TEST411 = "A07411.csv"
IRIS_TEST412 = "A07412.csv"
IRIS_TEST413 = "A07413.csv"
IRIS_TEST414 = "A07414.csv"
IRIS_TEST415 = "A07415.csv"
IRIS_TEST416 = "A07416.csv"

IRIS_TEST418 = "A07418.csv"

IRIS_TEST420 = "A07420.csv"

IRIS_TEST422 = "A07422.csv"
IRIS_TEST423 = "A07423.csv"
IRIS_TEST424 = "A07424.csv"
IRIS_TEST425 = "A07425.csv"
IRIS_TEST426 = "A07426.csv"
IRIS_TEST427 = "A07427.csv"
IRIS_TEST428 = "A07428.csv"
IRIS_TEST429 = "A07429.csv"

IRIS_TEST431 = "A07431.csv"
IRIS_TEST432 = "A07432.csv"
IRIS_TEST433 = "A07433.csv"
IRIS_TEST434 = "A07434.csv"
IRIS_TEST435 = "A07435.csv"
IRIS_TEST436 = "A07436.csv"
IRIS_TEST437 = "A07437.csv"

IRIS_TEST439 = "A07439.csv"


IRIS_TEST442 = "A07442.csv"
IRIS_TEST443 = "A07443.csv"
IRIS_TEST444 = "A07444.csv"

IRIS_TEST447 = "A07447.csv"

IRIS_TEST449 = "A07449.csv"

IRIS_TEST451 = "A07451.csv"
IRIS_TEST452 = "A07452.csv"
IRIS_TEST453 = "A07453.csv"
IRIS_TEST454 = "A07454.csv"
IRIS_TEST455 = "A07455.csv"

IRIS_TEST457 = "A07457.csv"
IRIS_TEST458 = "A07458.csv"
IRIS_TEST459 = "A07459.csv"

IRIS_TEST461 = "A07461.csv"

IRIS_TEST463 = "A07463.csv"

IRIS_TEST466 = "A07466.csv"
IRIS_TEST467 = "A07467.csv"
IRIS_TEST468 = "A07468.csv"
IRIS_TEST469 = "A07469.csv"
IRIS_TEST470 = "A07470.csv"
IRIS_TEST471 = "A07471.csv"
IRIS_TEST472 = "A07472.csv"
IRIS_TEST473 = "A07473.csv"
IRIS_TEST474 = "A07474.csv"
IRIS_TEST475 = "A07475.csv"
IRIS_TEST476 = "A07476.csv"
IRIS_TEST477 = "A07477.csv"
IRIS_TEST478 = "A07478.csv"
IRIS_TEST479 = "A07479.csv"
IRIS_TEST480 = "A07480.csv"

IRIS_TEST482 = "A07482.csv"
IRIS_TEST483 = "A07483.csv"

IRIS_TEST487 = "A07487.csv"
IRIS_TEST488 = "A07488.csv"

IRIS_TEST490 = "A07490.csv"
IRIS_TEST491 = "A07491.csv"

IRIS_TEST494 = "A07494.csv"
IRIS_TEST495 = "A07495.csv"
IRIS_TEST496 = "A07496.csv"

IRIS_TEST498 = "A07498.csv"
IRIS_TEST499 = "A07499.csv"

IRIS_TEST501 = "A07501.csv"
IRIS_TEST502 = "A07502.csv"
IRIS_TEST503 = "A07503.csv"
IRIS_TEST504 = "A07504.csv"
IRIS_TEST505 = "A07505.csv"

IRIS_TEST507 = "A07507.csv"
IRIS_TEST508 = "A07508.csv"
IRIS_TEST509 = "A07509.csv"

IRIS_TEST511 = "A07511.csv"
IRIS_TEST512 = "A07512.csv"
IRIS_TEST513 = "A07513.csv"
IRIS_TEST514 = "A07514.csv"
IRIS_TEST515 = "A07515.csv"
IRIS_TEST516 = "A07516.csv"

IRIS_TEST518 = "A07518.csv"
IRIS_TEST519 = "A07519.csv"
IRIS_TEST520 = "A07520.csv"
IRIS_TEST521 = "A07521.csv"

IRIS_TEST523 = "A07523.csv"

IRIS_TEST525 = "A07525.csv"

IRIS_TEST528 = "A07528.csv"
IRIS_TEST529 = "A07529.csv"
IRIS_TEST530 = "A07530.csv"

IRIS_TEST532 = "A07532.csv"

IRIS_TEST534 = "A07534.csv"
IRIS_TEST535 = "A07535.csv"
IRIS_TEST536 = "A07536.csv"

IRIS_TEST538 = "A07538.csv"



IRIS_TEST543 = "A07543.csv"
IRIS_TEST544 = "A07544.csv"
IRIS_TEST545 = "A07545.csv"
IRIS_TEST546 = "A07546.csv"

IRIS_TEST548 = "A07548.csv"

IRIS_TEST551 = "A07551.csv"
IRIS_TEST552 = "A07552.csv"
IRIS_TEST553 = "A07553.csv"
IRIS_TEST554 = "A07554.csv"
IRIS_TEST555 = "A07555.csv"

IRIS_TEST557 = "A07557.csv"
IRIS_TEST558 = "A07558.csv"
IRIS_TEST559 = "A07559.csv"

IRIS_TEST561 = "A07561.csv"
IRIS_TEST562 = "A07562.csv"
IRIS_TEST563 = "A07563.csv"

IRIS_TEST566 = "A07566.csv"

IRIS_TEST568 = "A07568.csv"
IRIS_TEST569 = "A07569.csv"

IRIS_TEST571 = "A07571.csv"

IRIS_TEST573 = "A07573.csv"

IRIS_TEST575 = "A07575.csv"
IRIS_TEST576 = "A07576.csv"

IRIS_TEST578 = "A07578.csv"
IRIS_TEST579 = "A07579.csv"

IRIS_TEST582 = "A07582.csv"

IRIS_TEST584 = "A07584.csv"
IRIS_TEST585 = "A07585.csv"
IRIS_TEST586 = "A07586.csv"

IRIS_TEST588 = "A07588.csv"
IRIS_TEST589 = "A07589.csv"
IRIS_TEST590 = "A07590.csv"
IRIS_TEST591 = "A07591.csv"
IRIS_TEST592 = "A07592.csv"
IRIS_TEST593 = "A07593.csv"
IRIS_TEST594 = "A07594.csv"
IRIS_TEST595 = "A07595.csv"
IRIS_TEST596 = "A07596.csv"

IRIS_TEST598 = "A07598.csv"
IRIS_TEST599 = "A07599.csv"
IRIS_TEST600 = "A07600.csv"
IRIS_TEST601 = "A07601.csv"


IRIS_TEST604 = "A07604.csv"


IRIS_TEST607 = "A07607.csv"
IRIS_TEST608 = "A07608.csv"
IRIS_TEST609 = "A07609.csv"

IRIS_TEST611 = "A07611.csv"
IRIS_TEST612 = "A07612.csv"
IRIS_TEST613 = "A07613.csv"
IRIS_TEST614 = "A07614.csv"
IRIS_TEST615 = "A07615.csv"
IRIS_TEST616 = "A07616.csv"

IRIS_TEST619 = "A07619.csv"

IRIS_TEST621 = "A07621.csv"
IRIS_TEST622 = "A07622.csv"
IRIS_TEST623 = "A07623.csv"
IRIS_TEST624 = "A07624.csv"
IRIS_TEST625 = "A07625.csv"
IRIS_TEST626 = "A07626.csv"

IRIS_TEST629 = "A07629.csv"
IRIS_TEST630 = "A07630.csv"
IRIS_TEST631 = "A07631.csv"

IRIS_TEST634 = "A07634.csv"
IRIS_TEST635 = "A07635.csv"

IRIS_TEST639 = "A07639.csv"
IRIS_TEST640 = "A07640.csv"

IRIS_TEST642 = "A07642.csv"

IRIS_TEST644 = "A07644.csv"
IRIS_TEST645 = "A07645.csv"
IRIS_TEST646 = "A07646.csv"
IRIS_TEST647 = "A07647.csv"


IRIS_TEST650 = "A07650.csv"
IRIS_TEST651 = "A07651.csv"
IRIS_TEST652 = "A07652.csv"
IRIS_TEST653 = "A07653.csv"
IRIS_TEST654 = "A07654.csv"
IRIS_TEST655 = "A07655.csv"
IRIS_TEST656 = "A07656.csv"
IRIS_TEST657 = "A07657.csv"

IRIS_TEST660 = "A07660.csv"
IRIS_TEST661 = "A07661.csv"
IRIS_TEST662 = "A07662.csv"
IRIS_TEST663 = "A07663.csv"
IRIS_TEST664 = "A07664.csv"
IRIS_TEST665 = "A07665.csv"
IRIS_TEST666 = "A07666.csv"
IRIS_TEST667 = "A07667.csv"
IRIS_TEST668 = "A07668.csv"
IRIS_TEST669 = "A07669.csv"

IRIS_TEST671 = "A07671.csv"

IRIS_TEST673 = "A07673.csv"

IRIS_TEST675 = "A07675.csv"
IRIS_TEST676 = "A07676.csv"
IRIS_TEST677 = "A07677.csv"


IRIS_TEST680 = "A07680.csv"
IRIS_TEST681 = "A07681.csv"
IRIS_TEST682 = "A07682.csv"
IRIS_TEST683 = "A07683.csv"
IRIS_TEST684 = "A07684.csv"
IRIS_TEST685 = "A07685.csv"

IRIS_TEST687 = "A07687.csv"
IRIS_TEST688 = "A07688.csv"

IRIS_TEST690 = "A07690.csv"

IRIS_TEST692 = "A07692.csv"
IRIS_TEST693 = "A07693.csv"
IRIS_TEST694 = "A07694.csv"
IRIS_TEST695 = "A07695.csv"

IRIS_TEST697 = "A07697.csv"
IRIS_TEST698 = "A07698.csv"
IRIS_TEST699 = "A07699.csv"
IRIS_TEST700 = "A07700.csv"



IRIS_TEST704 = "A07704.csv"
IRIS_TEST705 = "A07705.csv"
IRIS_TEST706 = "A07706.csv"
IRIS_TEST707 = "A07707.csv"

IRIS_TEST709 = "A07709.csv"
IRIS_TEST710 = "A07710.csv"

IRIS_TEST712 = "A07712.csv"

IRIS_TEST714 = "A07714.csv"
IRIS_TEST715 = "A07715.csv"
IRIS_TEST716 = "A07716.csv"
IRIS_TEST717 = "A07717.csv"
IRIS_TEST718 = "A07718.csv"
IRIS_TEST719 = "A07719.csv"

IRIS_TEST721 = "A07721.csv"
IRIS_TEST722 = "A07722.csv"

IRIS_TEST725 = "A07725.csv"

IRIS_TEST728 = "A07728.csv"
IRIS_TEST729 = "A07729.csv"
IRIS_TEST730 = "A07730.csv"

IRIS_TEST732 = "A07732.csv"

IRIS_TEST735 = "A07735.csv"
IRIS_TEST736 = "A07736.csv"

IRIS_TEST738 = "A07738.csv"
IRIS_TEST739 = "A07739.csv"


IRIS_TEST743 = "A07743.csv"
IRIS_TEST744 = "A07744.csv"
IRIS_TEST745 = "A07745.csv"
IRIS_TEST746 = "A07746.csv"
IRIS_TEST747 = "A07747.csv"
IRIS_TEST748 = "A07748.csv"
IRIS_TEST749 = "A07749.csv"
IRIS_TEST750 = "A07750.csv"
IRIS_TEST751 = "A07751.csv"

IRIS_TEST753 = "A07753.csv"

IRIS_TEST755 = "A07755.csv"

IRIS_TEST757 = "A07757.csv"
IRIS_TEST758 = "A07758.csv"
IRIS_TEST759 = "A07759.csv"

IRIS_TEST761 = "A07761.csv"
IRIS_TEST762 = "A07762.csv"
IRIS_TEST763 = "A07763.csv"
IRIS_TEST764 = "A07764.csv"
IRIS_TEST765 = "A07765.csv"
IRIS_TEST766 = "A07766.csv"
IRIS_TEST767 = "A07767.csv"

IRIS_TEST769 = "A07769.csv"
IRIS_TEST770 = "A07770.csv"
IRIS_TEST771 = "A07771.csv"


IRIS_TEST774 = "A07774.csv"
IRIS_TEST775 = "A07775.csv"

IRIS_TEST778 = "A07778.csv"

IRIS_TEST780 = "A07780.csv"

IRIS_TEST782 = "A07782.csv"
IRIS_TEST783 = "A07783.csv"
IRIS_TEST784 = "A07784.csv"

IRIS_TEST788 = "A07788.csv"

IRIS_TEST791 = "A07791.csv"
IRIS_TEST792 = "A07792.csv"
IRIS_TEST793 = "A07793.csv"

IRIS_TEST795 = "A07795.csv"

IRIS_TEST798 = "A07798.csv"

IRIS_TEST800 = "A07800.csv"


IRIS_TEST803 = "A07803.csv"
IRIS_TEST804 = "A07804.csv"
IRIS_TEST805 = "A07805.csv"
IRIS_TEST806 = "A07806.csv"
IRIS_TEST807 = "A07807.csv"

IRIS_TEST810 = "A07810.csv"
IRIS_TEST811 = "A07811.csv"
IRIS_TEST812 = "A07812.csv"
IRIS_TEST813 = "A07813.csv"
IRIS_TEST814 = "A07814.csv"

IRIS_TEST817 = "A07817.csv"
IRIS_TEST818 = "A07818.csv"
IRIS_TEST819 = "A07819.csv"
IRIS_TEST820 = "A07820.csv"

IRIS_TEST822 = "A07822.csv"
IRIS_TEST823 = "A07823.csv"
IRIS_TEST824 = "A07824.csv"

IRIS_TEST826 = "A07826.csv"

IRIS_TEST828 = "A07828.csv"
IRIS_TEST829 = "A07829.csv"

IRIS_TEST832 = "A07832.csv"

IRIS_TEST834 = "A07834.csv"
IRIS_TEST835 = "A07835.csv"
IRIS_TEST836 = "A07836.csv"
IRIS_TEST837 = "A07837.csv"
IRIS_TEST838 = "A07838.csv"
IRIS_TEST839 = "A07839.csv"

IRIS_TEST841 = "A07841.csv"
IRIS_TEST842 = "A07842.csv"
IRIS_TEST843 = "A07843.csv"
IRIS_TEST844 = "A07844.csv"

IRIS_TEST846 = "A07846.csv"
IRIS_TEST847 = "A07847.csv"
IRIS_TEST848 = "A07848.csv"
IRIS_TEST849 = "A07849.csv"

IRIS_TEST851 = "A07851.csv"
IRIS_TEST852 = "A07852.csv"

IRIS_TEST854 = "A07854.csv"
IRIS_TEST855 = "A07855.csv"
IRIS_TEST856 = "A07856.csv"

IRIS_TEST858 = "A07858.csv"
IRIS_TEST859 = "A07859.csv"
IRIS_TEST860 = "A07860.csv"
IRIS_TEST861 = "A07861.csv"
IRIS_TEST862 = "A07862.csv"
IRIS_TEST863 = "A07863.csv"
IRIS_TEST864 = "A07864.csv"

IRIS_TEST866 = "A07866.csv"

IRIS_TEST868 = "A07868.csv"

IRIS_TEST870 = "A07870.csv"
IRIS_TEST871 = "A07871.csv"
IRIS_TEST872 = "A07872.csv"
IRIS_TEST873 = "A07873.csv"

IRIS_TEST875 = "A07875.csv"
IRIS_TEST876 = "A07876.csv"
IRIS_TEST877 = "A07877.csv"



IRIS_TEST882 = "A07882.csv"

IRIS_TEST884 = "A07884.csv"
IRIS_TEST885 = "A07885.csv"
IRIS_TEST886 = "A07886.csv"

IRIS_TEST888 = "A07888.csv"
IRIS_TEST889 = "A07889.csv"

IRIS_TEST893 = "A07893.csv"

IRIS_TEST896 = "A07896.csv"
IRIS_TEST897 = "A07897.csv"
IRIS_TEST898 = "A07898.csv"

IRIS_TEST901 = "A07901.csv"

IRIS_TEST903 = "A07903.csv"
IRIS_TEST904 = "A07904.csv"
IRIS_TEST905 = "A07905.csv"
IRIS_TEST906 = "A07906.csv"
IRIS_TEST907 = "A07907.csv"

IRIS_TEST909 = "A07909.csv"
IRIS_TEST910 = "A07910.csv"
IRIS_TEST911 = "A07911.csv"
IRIS_TEST912 = "A07912.csv"

IRIS_TEST916 = "A07916.csv"
IRIS_TEST917 = "A07917.csv"
IRIS_TEST918 = "A07918.csv"
IRIS_TEST919 = "A07919.csv"

IRIS_TEST922 = "A07922.csv"

IRIS_TEST924 = "A07924.csv"
IRIS_TEST925 = "A07925.csv"
IRIS_TEST926 = "A07926.csv"
IRIS_TEST927 = "A07927.csv"

IRIS_TEST929 = "A07929.csv"
IRIS_TEST930 = "A07930.csv"
IRIS_TEST931 = "A07931.csv"
IRIS_TEST932 = "A07932.csv"
IRIS_TEST933 = "A07933.csv"

IRIS_TEST935 = "A07935.csv"

IRIS_TEST937 = "A07937.csv"

IRIS_TEST941 = "A07941.csv"

IRIS_TEST943 = "A07943.csv"
IRIS_TEST944 = "A07944.csv"
IRIS_TEST945 = "A07945.csv"
IRIS_TEST946 = "A07946.csv"
IRIS_TEST947 = "A07947.csv"
IRIS_TEST948 = "A07948.csv"
IRIS_TEST949 = "A07949.csv"
IRIS_TEST950 = "A07950.csv"
IRIS_TEST951 = "A07951.csv"

IRIS_TEST953 = "A07953.csv"

IRIS_TEST955 = "A07955.csv"
IRIS_TEST956 = "A07956.csv"
IRIS_TEST957 = "A07957.csv"
IRIS_TEST958 = "A07958.csv"

IRIS_TEST960 = "A07960.csv"

IRIS_TEST962 = "A07962.csv"

IRIS_TEST964 = "A07964.csv"
IRIS_TEST965 = "A07965.csv"

IRIS_TEST967 = "A07967.csv"

IRIS_TEST969 = "A07969.csv"
IRIS_TEST970 = "A07970.csv"

IRIS_TEST972 = "A07972.csv"

IRIS_TEST974 = "A07974.csv"
IRIS_TEST975 = "A07975.csv"

IRIS_TEST979 = "A07979.csv"

IRIS_TEST981 = "A07981.csv"
IRIS_TEST982 = "A07982.csv"
IRIS_TEST983 = "A07983.csv"
IRIS_TEST984 = "A07984.csv"

IRIS_TEST987 = "A07987.csv"

IRIS_TEST989 = "A07989.csv"

IRIS_TEST991 = "A07991.csv"

IRIS_TEST993 = "A07993.csv"
IRIS_TEST994 = "A07994.csv"
IRIS_TEST995 = "A07995.csv"

IRIS_TEST997 = "A07997.csv"

IRIS_TEST999 = "A07999.csv"
IRIS_TEST1000 = "A08000.csv"
IRIS_TEST1001 = "A08001.csv"
IRIS_TEST1002 = "A08002.csv"
IRIS_TEST1003 = "A08003.csv"
IRIS_TEST1004 = "A08004.csv"

IRIS_TEST1006 = "A08006.csv"

IRIS_TEST1009 = "A08009.csv"

IRIS_TEST1011 = "A08011.csv"
IRIS_TEST1012 = "A08012.csv"
IRIS_TEST1013 = "A08013.csv"
IRIS_TEST1014 = "A08014.csv"
IRIS_TEST1015 = "A08015.csv"
IRIS_TEST1016 = "A08016.csv"

IRIS_TEST1018 = "A08018.csv"

IRIS_TEST1020 = "A08020.csv"

IRIS_TEST1022 = "A08022.csv"
IRIS_TEST1023 = "A08023.csv"

IRIS_TEST1025 = "A08025.csv"
IRIS_TEST1026 = "A08026.csv"

IRIS_TEST1028 = "A08028.csv"
IRIS_TEST1029 = "A08029.csv"

IRIS_TEST1031 = "A08031.csv"
IRIS_TEST1032 = "A08032.csv"
IRIS_TEST1033 = "A08033.csv"



IRIS_TEST1038 = "A08038.csv"


IRIS_TEST1041 = "A08041.csv"

IRIS_TEST1043 = "A08043.csv"
IRIS_TEST1044 = "A08044.csv"

IRIS_TEST1046 = "A08046.csv"

IRIS_TEST1049 = "A08049.csv"

IRIS_TEST1051 = "A08051.csv"
IRIS_TEST1052 = "A08052.csv"
IRIS_TEST1053 = "A08053.csv"

IRIS_TEST1055 = "A08055.csv"

IRIS_TEST1057 = "A08057.csv"

IRIS_TEST1062 = "A08062.csv"
IRIS_TEST1063 = "A08063.csv"
IRIS_TEST1064 = "A08064.csv"
IRIS_TEST1065 = "A08065.csv"
IRIS_TEST1066 = "A08066.csv"
IRIS_TEST1067 = "A08067.csv"
IRIS_TEST1068 = "A08068.csv"
IRIS_TEST1069 = "A08069.csv"

IRIS_TEST1072 = "A08072.csv"
IRIS_TEST1073 = "A08073.csv"
IRIS_TEST1074 = "A08074.csv"
IRIS_TEST1075 = "A08075.csv"

IRIS_TEST1077 = "A08077.csv"
IRIS_TEST1078 = "A08078.csv"
IRIS_TEST1079 = "A08079.csv"
IRIS_TEST1080 = "A08080.csv"

IRIS_TEST1082 = "A08082.csv"
IRIS_TEST1083 = "A08083.csv"
IRIS_TEST1084 = "A08084.csv"
IRIS_TEST1085 = "A08085.csv"

IRIS_TEST1088 = "A08088.csv"
IRIS_TEST1089 = "A08089.csv"

IRIS_TEST1091 = "A08091.csv"
IRIS_TEST1092 = "A08092.csv"

IRIS_TEST1094 = "A08094.csv"
IRIS_TEST1095 = "A08095.csv"

IRIS_TEST1097 = "A08097.csv"
IRIS_TEST1098 = "A08098.csv"
IRIS_TEST1099 = "A08099.csv"
IRIS_TEST1100 = "A08100.csv"

IRIS_TEST1102 = "A08102.csv"
IRIS_TEST1103 = "A08103.csv"

IRIS_TEST1105 = "A08105.csv"
IRIS_TEST1106 = "A08106.csv"
IRIS_TEST1107 = "A08107.csv"
IRIS_TEST1108 = "A08108.csv"
IRIS_TEST1109 = "A08109.csv"
IRIS_TEST1110 = "A08110.csv"
IRIS_TEST1111 = "A08111.csv"

IRIS_TEST1113 = "A08113.csv"

IRIS_TEST1115 = "A08115.csv"
IRIS_TEST1116 = "A08116.csv"
IRIS_TEST1117 = "A08117.csv"

IRIS_TEST1119 = "A08119.csv"
IRIS_TEST1120 = "A08120.csv"
IRIS_TEST1121 = "A08121.csv"
IRIS_TEST1122 = "A08122.csv"
IRIS_TEST1123 = "A08123.csv"
IRIS_TEST1124 = "A08124.csv"
IRIS_TEST1125 = "A08125.csv"

IRIS_TEST1127 = "A08127.csv"
IRIS_TEST1128 = "A08128.csv"
IRIS_TEST1129 = "A08129.csv"
IRIS_TEST1130 = "A08130.csv"
IRIS_TEST1131 = "A08131.csv"
IRIS_TEST1132 = "A08132.csv"


IRIS_TEST1135 = "A08135.csv"
IRIS_TEST1136 = "A08136.csv"
IRIS_TEST1137 = "A08137.csv"
IRIS_TEST1138 = "A08138.csv"

IRIS_TEST1140 = "A08140.csv"
IRIS_TEST1141 = "A08141.csv"

IRIS_TEST1143 = "A08143.csv"
IRIS_TEST1144 = "A08144.csv"
IRIS_TEST1145 = "A08145.csv"


IRIS_TEST1150 = "A08150.csv"
IRIS_TEST1151 = "A08151.csv"
IRIS_TEST1152 = "A08152.csv"

IRIS_TEST1154 = "A08154.csv"
IRIS_TEST1155 = "A08155.csv"
IRIS_TEST1156 = "A08156.csv"
IRIS_TEST1157 = "A08157.csv"
IRIS_TEST1158 = "A08158.csv"

IRIS_TEST1161 = "A08161.csv"
IRIS_TEST1162 = "A08162.csv"

IRIS_TEST1165 = "A08165.csv"

IRIS_TEST1168 = "A08168.csv"
IRIS_TEST1169 = "A08169.csv"
IRIS_TEST1170 = "A08170.csv"
IRIS_TEST1171 = "A08171.csv"
IRIS_TEST1172 = "A08172.csv"
IRIS_TEST1173 = "A08173.csv"
IRIS_TEST1174 = "A08174.csv"

IRIS_TEST1177 = "A08177.csv"
IRIS_TEST1178 = "A08178.csv"

IRIS_TEST1180 = "A08180.csv"

IRIS_TEST1182 = "A08182.csv"
IRIS_TEST1183 = "A08183.csv"
IRIS_TEST1184 = "A08184.csv"

IRIS_TEST1186 = "A08186.csv"
IRIS_TEST1187 = "A08187.csv"
IRIS_TEST1188 = "A08188.csv"
IRIS_TEST1189 = "A08189.csv"

IRIS_TEST1191 = "A08191.csv"
IRIS_TEST1192 = "A08192.csv"
IRIS_TEST1193 = "A08193.csv"


IRIS_TEST1196 = "A08196.csv"
IRIS_TEST1197 = "A08197.csv"
IRIS_TEST1198 = "A08198.csv"
IRIS_TEST1199 = "A08199.csv"

IRIS_TEST1201 = "A08201.csv"
IRIS_TEST1202 = "A08202.csv"

IRIS_TEST1204 = "A08204.csv"
IRIS_TEST1205 = "A08205.csv"
IRIS_TEST1206 = "A08206.csv"
IRIS_TEST1207 = "A08207.csv"


IRIS_TEST1212 = "A08212.csv"

IRIS_TEST1214 = "A08214.csv"
IRIS_TEST1215 = "A08215.csv"

IRIS_TEST1218 = "A08218.csv"
IRIS_TEST1219 = "A08219.csv"
IRIS_TEST1220 = "A08220.csv"

IRIS_TEST1222 = "A08222.csv"
IRIS_TEST1223 = "A08223.csv"
IRIS_TEST1224 = "A08224.csv"
IRIS_TEST1225 = "A08225.csv"
IRIS_TEST1226 = "A08226.csv"
IRIS_TEST1227 = "A08227.csv"
IRIS_TEST1228 = "A08228.csv"


IRIS_TEST1231 = "A08231.csv"
IRIS_TEST1232 = "A08232.csv"
IRIS_TEST1233 = "A08233.csv"
IRIS_TEST1234 = "A08234.csv"
IRIS_TEST1235 = "A08235.csv"
IRIS_TEST1236 = "A08236.csv"
IRIS_TEST1237 = "A08237.csv"
IRIS_TEST1238 = "A08238.csv"
IRIS_TEST1239 = "A08239.csv"
IRIS_TEST1240 = "A08240.csv"

IRIS_TEST1242 = "A08242.csv"
IRIS_TEST1243 = "A08243.csv"
IRIS_TEST1244 = "A08244.csv"
IRIS_TEST1245 = "A08245.csv"

IRIS_TEST1248 = "A08248.csv"


IRIS_TEST1252 = "A08252.csv"

IRIS_TEST1254 = "A08254.csv"
IRIS_TEST1255 = "A08255.csv"

IRIS_TEST1257 = "A08257.csv"
IRIS_TEST1258 = "A08258.csv"
IRIS_TEST1259 = "A08259.csv"
IRIS_TEST1260 = "A08260.csv"
IRIS_TEST1261 = "A08261.csv"

IRIS_TEST1263 = "A08263.csv"
IRIS_TEST1264 = "A08264.csv"
IRIS_TEST1265 = "A08265.csv"

IRIS_TEST1270 = "A08270.csv"
IRIS_TEST1271 = "A08271.csv"
IRIS_TEST1272 = "A08272.csv"

IRIS_TEST1274 = "A08274.csv"
IRIS_TEST1275 = "A08275.csv"

IRIS_TEST1277 = "A08277.csv"

IRIS_TEST1279 = "A08279.csv"
IRIS_TEST1280 = "A08280.csv"
IRIS_TEST1281 = "A08281.csv"
IRIS_TEST1282 = "A08282.csv"
IRIS_TEST1283 = "A08283.csv"
IRIS_TEST1284 = "A08284.csv"

IRIS_TEST1286 = "A08286.csv"
IRIS_TEST1287 = "A08287.csv"
IRIS_TEST1288 = "A08288.csv"
IRIS_TEST1289 = "A08289.csv"
IRIS_TEST1290 = "A08290.csv"

IRIS_TEST1295 = "A08295.csv"
IRIS_TEST1296 = "A08296.csv"
IRIS_TEST1297 = "A08297.csv"
IRIS_TEST1298 = "A08298.csv"

IRIS_TEST1300 = "A08300.csv"

IRIS_TEST1302 = "A08302.csv"

IRIS_TEST1304 = "A08304.csv"
IRIS_TEST1305 = "A08305.csv"
IRIS_TEST1306 = "A08306.csv"
IRIS_TEST1307 = "A08307.csv"
IRIS_TEST1308 = "A08308.csv"

IRIS_TEST1315 = "A08315.csv"
IRIS_TEST1316 = "A08316.csv"

IRIS_TEST1318 = "A08318.csv"
IRIS_TEST1319 = "A08319.csv"

IRIS_TEST1321 = "A08321.csv"
IRIS_TEST1322 = "A08322.csv"
IRIS_TEST1323 = "A08323.csv"
IRIS_TEST1324 = "A08324.csv"
IRIS_TEST1325 = "A08325.csv"
IRIS_TEST1326 = "A08326.csv"
IRIS_TEST1327 = "A08327.csv"
IRIS_TEST1328 = "A08328.csv"

IRIS_TEST1330 = "A08330.csv"

IRIS_TEST1333 = "A08333.csv"
IRIS_TEST1334 = "A08334.csv"


IRIS_TEST1337 = "A08337.csv"
IRIS_TEST1338 = "A08338.csv"

IRIS_TEST1340 = "A08340.csv"
IRIS_TEST1341 = "A08341.csv"
IRIS_TEST1342 = "A08342.csv"

IRIS_TEST1344 = "A08344.csv"
IRIS_TEST1345 = "A08345.csv"
IRIS_TEST1346 = "A08346.csv"
IRIS_TEST1347 = "A08347.csv"
IRIS_TEST1348 = "A08348.csv"
IRIS_TEST1349 = "A08349.csv"
IRIS_TEST1350 = "A08350.csv"
IRIS_TEST1351 = "A08351.csv"
IRIS_TEST1352 = "A08352.csv"
IRIS_TEST1353 = "A08353.csv"
IRIS_TEST1354 = "A08354.csv"
IRIS_TEST1355 = "A08355.csv"
IRIS_TEST1356 = "A08356.csv"
IRIS_TEST1357 = "A08357.csv"
IRIS_TEST1358 = "A08358.csv"

IRIS_TEST1360 = "A08360.csv"

IRIS_TEST1362 = "A08362.csv"
IRIS_TEST1363 = "A08363.csv"
IRIS_TEST1364 = "A08364.csv"

IRIS_TEST1366 = "A08366.csv"
IRIS_TEST1367 = "A08367.csv"
IRIS_TEST1368 = "A08368.csv"
IRIS_TEST1369 = "A08369.csv"
IRIS_TEST1370 = "A08370.csv"
IRIS_TEST1371 = "A08371.csv"
IRIS_TEST1372 = "A08372.csv"
IRIS_TEST1373 = "A08373.csv"
IRIS_TEST1374 = "A08374.csv"

IRIS_TEST1376 = "A08376.csv"
IRIS_TEST1377 = "A08377.csv"

IRIS_TEST1379 = "A08379.csv"
IRIS_TEST1380 = "A08380.csv"
IRIS_TEST1381 = "A08381.csv"
IRIS_TEST1382 = "A08382.csv"

IRIS_TEST1384 = "A08384.csv"
IRIS_TEST1385 = "A08385.csv"

IRIS_TEST1387 = "A08387.csv"

IRIS_TEST1390 = "A08390.csv"

IRIS_TEST1392 = "A08392.csv"
IRIS_TEST1393 = "A08393.csv"
IRIS_TEST1394 = "A08394.csv"
IRIS_TEST1395 = "A08395.csv"

IRIS_TEST1397 = "A08397.csv"

IRIS_TEST1403 = "A08403.csv"

IRIS_TEST1405 = "A08405.csv"
IRIS_TEST1406 = "A08406.csv"

IRIS_TEST1408 = "A08408.csv"

IRIS_TEST1411 = "A08411.csv"

IRIS_TEST1413 = "A08413.csv"
IRIS_TEST1414 = "A08414.csv"

IRIS_TEST1416 = "A08416.csv"
IRIS_TEST1417 = "A08417.csv"
IRIS_TEST1418 = "A08418.csv"
IRIS_TEST1419 = "A08419.csv"
IRIS_TEST1420 = "A08420.csv"
IRIS_TEST1421 = "A08421.csv"
IRIS_TEST1422 = "A08422.csv"
IRIS_TEST1423 = "A08423.csv"
IRIS_TEST1424 = "A08424.csv"

IRIS_TEST1426 = "A08426.csv"

IRIS_TEST1429 = "A08429.csv"
IRIS_TEST1430 = "A08430.csv"

IRIS_TEST1435 = "A08435.csv"
IRIS_TEST1436 = "A08436.csv"

IRIS_TEST1438 = "A08438.csv"

IRIS_TEST1440 = "A08440.csv"
IRIS_TEST1441 = "A08441.csv"
IRIS_TEST1442 = "A08442.csv"
IRIS_TEST1443 = "A08443.csv"
IRIS_TEST1444 = "A08444.csv"
IRIS_TEST1445 = "A08445.csv"
IRIS_TEST1446 = "A08446.csv"
IRIS_TEST1447 = "A08447.csv"
IRIS_TEST1448 = "A08448.csv"
IRIS_TEST1449 = "A08449.csv"

IRIS_TEST1451 = "A08451.csv"

IRIS_TEST1454 = "A08454.csv"
IRIS_TEST1455 = "A08455.csv"

IRIS_TEST1457 = "A08457.csv"

IRIS_TEST1459 = "A08459.csv"
IRIS_TEST1460 = "A08460.csv"
IRIS_TEST1461 = "A08461.csv"
IRIS_TEST1462 = "A08462.csv"

IRIS_TEST1465 = "A08465.csv"
IRIS_TEST1466 = "A08466.csv"
IRIS_TEST1467 = "A08467.csv"

IRIS_TEST1469 = "A08469.csv"

IRIS_TEST1472 = "A08472.csv"

IRIS_TEST1474 = "A08474.csv"
IRIS_TEST1475 = "A08475.csv"
IRIS_TEST1476 = "A08476.csv"
IRIS_TEST1477 = "A08477.csv"

IRIS_TEST1480 = "A08480.csv"

IRIS_TEST1482 = "A08482.csv"
IRIS_TEST1483 = "A08483.csv"

IRIS_TEST1485 = "A08485.csv"
IRIS_TEST1486 = "A08486.csv"

IRIS_TEST1488 = "A08488.csv"
IRIS_TEST1489 = "A08489.csv"

IRIS_TEST1491 = "A08491.csv"

IRIS_TEST1494 = "A08494.csv"
IRIS_TEST1495 = "A08495.csv"
IRIS_TEST1496 = "A08496.csv"
IRIS_TEST1497 = "A08497.csv"

IRIS_TEST1500 = "A08500.csv"

IRIS_TEST1502 = "A08502.csv"
IRIS_TEST1503 = "A08503.csv"

IRIS_TEST1505 = "A08505.csv"
IRIS_TEST1506 = "A08506.csv"
IRIS_TEST1507 = "A08507.csv"
IRIS_TEST1508 = "A08508.csv"
IRIS_TEST1509 = "A08509.csv"

IRIS_TEST1512 = "A08512.csv"
IRIS_TEST1513 = "A08513.csv"
IRIS_TEST1514 = "A08514.csv"
IRIS_TEST1515 = "A08515.csv"

IRIS_TEST1517 = "A08517.csv"
IRIS_TEST1518 = "A08518.csv"


IRIS_TEST1522 = "A08522.csv"
IRIS_TEST1523 = "A08523.csv"
IRIS_TEST1524 = "A08524.csv"

IRIS_TEST1526 = "A08526.csv"
IRIS_TEST1527 = "A08527.csv"
IRIS_TEST1528 = "A08528.csv"


test_set2=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST2,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set4=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST4,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set7=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST7,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set8=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST8,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set9=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST9,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set10=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST10,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set11=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST11,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set12=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST12,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set15=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST15,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set16=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST16,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set19=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST19,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set20=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST20,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set21=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST21,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set22=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST22,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set23=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST23,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set24=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST24,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set25=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST25,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set26=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST26,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set28=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST28,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)





test_set32=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST32,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set33=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST33,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set34=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST34,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set35=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST35,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set36=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST36,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set37=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST37,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set39=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST39,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set40=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST40,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set41=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST41,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set42=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST42,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set43=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST43,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set44=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST44,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set45=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST45,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set47=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST47,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set48=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST48,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set50=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST50,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set51=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST51,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set52=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST52,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set53=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST53,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set54=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST54,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set55=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST55,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set56=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST56,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set57=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST57,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set58=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST58,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set59=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST59,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set60=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST60,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set63=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST63,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set65=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST65,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)




test_set70=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST70,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set73=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST73,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set74=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST74,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set75=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST75,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set77=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST77,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set78=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST78,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set79=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST79,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set80=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST80,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set81=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST81,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set82=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST82,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set85=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST85,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set86=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST86,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set88=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST88,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set89=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST89,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set90=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST90,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set92=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST92,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set94=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST94,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set95=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST95,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set96=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST96,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set97=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST97,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set98=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST98,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set100=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST100,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set101=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST101,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set102=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST102,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set103=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST103,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set104=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST104,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set105=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST105,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set106=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST106,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set107=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST107,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set108=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST108,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set109=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST109,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set110=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST110,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set111=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST111,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set112=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST112,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set113=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST113,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set114=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST114,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set115=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST115,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set116=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST116,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set117=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST117,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set118=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST118,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set120=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST120,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set121=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST121,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set122=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST122,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set123=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST123,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set124=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST124,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set125=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST125,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set126=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST126,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set127=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST127,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set128=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST128,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set129=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST129,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set130=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST130,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set131=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST131,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)





test_set134=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST134,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)





test_set140=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST140,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set141=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST141,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set142=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST142,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set143=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST143,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set146=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST146,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set147=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST147,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set149=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST149,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set151=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST151,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set152=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST152,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set153=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST153,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)





test_set158=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST158,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set160=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST160,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set161=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST161,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set163=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST163,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set164=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST164,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set165=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST165,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set167=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST167,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set168=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST168,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set169=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST169,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set170=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST170,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set173=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST173,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set174=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST174,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set175=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST175,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set176=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST176,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set178=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST178,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set180=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST180,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set181=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST181,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set182=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST182,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set183=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST183,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set184=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST184,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set186=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST186,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set188=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST188,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set189=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST189,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set190=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST190,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set191=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST191,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set192=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST192,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set193=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST193,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set196=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST196,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set197=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST197,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set198=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST198,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set199=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST199,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set200=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST200,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set201=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST201,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set204=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST204,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set205=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST205,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set206=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST206,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set207=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST207,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set209=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST209,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set210=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST210,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set211=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST211,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set212=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST212,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set216=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST216,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set218=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST218,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set220=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST220,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set221=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST221,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set222=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST222,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set223=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST223,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set224=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST224,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set225=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST225,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set227=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST227,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set228=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST228,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set230=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST230,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set231=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST231,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set232=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST232,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set234=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST234,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set235=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST235,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set236=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST236,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set238=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST238,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set239=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST239,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set241=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST241,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set242=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST242,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set243=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST243,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set244=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST244,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set246=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST246,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set248=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST248,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set250=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST250,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set253=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST253,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set255=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST255,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set256=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST256,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set257=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST257,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set258=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST258,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set259=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST259,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set260=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST260,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set262=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST262,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set264=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST264,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set266=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST266,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set267=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST267,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set268=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST268,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set269=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST269,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set270=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST270,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set272=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST272,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set273=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST273,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set275=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST275,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set276=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST276,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set278=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST278,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set279=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST279,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set281=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST281,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set282=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST282,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set284=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST284,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set285=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST285,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set287=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST287,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set288=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST288,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)




test_set291=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST291,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set293=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST293,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set294=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST294,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set295=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST295,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set296=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST296,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set298=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST298,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set299=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST299,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set300=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST300,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set301=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST301,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set303=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST303,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set304=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST304,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set305=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST305,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set307=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST307,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set309=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST309,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set310=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST310,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set311=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST311,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set312=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST312,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set313=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST313,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set315=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST315,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set317=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST317,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set318=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST318,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set319=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST319,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set323=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST323,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set324=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST324,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set325=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST325,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set326=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST326,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set327=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST327,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set330=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST330,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set331=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST331,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set332=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST332,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set333=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST333,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set334=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST334,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set335=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST335,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set336=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST336,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set337=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST337,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set339=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST339,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set340=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST340,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set341=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST341,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set343=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST343,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set344=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST344,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set345=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST345,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set346=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST346,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set347=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST347,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set349=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST349,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set351=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST351,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set352=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST352,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set353=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST353,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set354=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST354,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set356=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST356,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set357=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST357,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set359=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST359,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set360=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST360,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set361=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST361,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set362=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST362,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set364=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST364,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set365=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST365,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set366=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST366,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set368=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST368,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set369=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST369,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set370=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST370,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set371=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST371,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set372=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST372,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set373=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST373,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set374=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST374,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set375=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST375,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set376=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST376,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set377=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST377,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set378=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST378,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set379=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST379,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set380=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST380,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set381=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST381,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set383=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST383,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set384=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST384,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set385=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST385,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set386=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST386,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set389=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST389,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set390=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST390,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set391=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST391,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set392=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST392,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set393=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST393,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set394=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST394,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set396=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST396,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set397=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST397,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set398=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST398,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set399=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST399,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set400=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST400,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set401=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST401,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set402=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST402,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set403=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST403,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set404=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST404,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set406=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST406,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set407=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST407,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set410=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST410,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set411=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST411,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set412=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST412,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set413=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST413,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set414=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST414,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set415=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST415,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set416=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST416,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set418=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST418,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set420=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST420,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set422=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST422,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set423=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST423,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set424=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST424,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set425=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST425,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set426=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST426,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set427=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST427,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set428=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST428,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set429=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST429,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set431=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST431,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set432=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST432,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set433=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST433,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set434=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST434,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set435=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST435,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set436=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST436,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set437=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST437,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set439=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST439,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)





test_set442=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST442,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set443=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST443,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set444=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST444,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set447=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST447,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set449=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST449,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set451=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST451,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set452=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST452,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set453=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST453,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set454=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST454,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set455=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST455,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set457=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST457,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set458=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST458,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set459=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST459,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set461=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST461,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set463=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST463,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)




test_set466=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST466,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set467=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST467,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set468=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST468,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set469=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST469,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set470=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST470,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set471=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST471,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set472=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST472,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set473=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST473,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set474=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST474,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set475=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST475,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set476=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST476,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set477=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST477,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set478=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST478,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set479=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST479,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set480=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST480,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set482=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST482,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set483=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST483,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set487=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST487,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set488=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST488,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set490=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST490,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set491=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST491,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set494=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST494,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set495=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST495,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set496=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST496,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set498=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST498,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set499=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST499,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set501=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST501,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set502=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST502,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set503=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST503,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set504=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST504,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set505=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST505,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set507=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST507,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set508=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST508,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set509=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST509,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set511=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST511,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set512=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST512,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set513=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST513,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set514=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST514,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set515=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST515,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set516=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST516,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set518=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST518,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set519=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST519,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set520=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST520,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set521=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST521,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set523=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST523,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set525=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST525,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)




test_set528=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST528,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set529=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST529,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set530=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST530,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set532=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST532,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set534=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST534,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set535=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST535,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set536=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST536,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set538=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST538,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)







test_set543=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST543,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set544=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST544,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set545=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST545,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set546=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST546,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set548=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST548,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)





test_set551=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST551,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set552=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST552,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set553=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST553,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set554=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST554,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set555=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST555,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set557=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST557,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set558=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST558,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set559=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST559,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set561=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST561,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set562=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST562,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set563=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST563,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)




test_set566=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST566,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set568=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST568,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set569=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST569,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set571=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST571,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set573=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST573,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set575=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST575,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set576=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST576,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set578=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST578,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set579=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST579,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)




test_set582=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST582,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set584=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST584,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set585=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST585,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set586=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST586,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set588=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST588,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set589=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST589,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set590=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST590,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set591=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST591,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set592=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST592,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set593=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST593,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set594=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST594,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set595=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST595,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set596=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST596,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set598=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST598,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set599=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST599,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set600=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST600,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set601=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST601,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)




test_set604=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST604,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set607=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST607,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set608=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST608,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set609=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST609,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set611=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST611,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set612=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST612,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set613=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST613,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set614=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST614,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set615=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST615,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set616=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST616,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set619=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST619,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set621=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST621,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set622=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST622,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set623=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST623,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set624=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST624,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set625=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST625,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set626=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST626,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)





test_set629=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST629,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set630=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST630,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set631=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST631,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set634=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST634,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set635=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST635,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set639=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST639,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set640=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST640,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set642=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST642,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set644=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST644,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set645=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST645,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set646=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST646,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set647=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST647,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)




test_set650=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST650,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set651=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST651,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set652=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST652,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set653=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST653,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set654=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST654,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set655=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST655,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set656=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST656,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set657=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST657,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set660=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST660,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set661=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST661,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set662=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST662,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set663=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST663,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set664=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST664,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set665=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST665,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set666=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST666,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set667=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST667,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set668=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST668,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set669=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST669,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set671=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST671,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set673=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST673,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set675=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST675,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set676=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST676,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set677=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST677,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set680=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST680,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set681=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST681,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set682=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST682,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set683=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST683,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set684=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST684,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set685=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST685,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set687=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST687,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set688=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST688,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set690=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST690,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set692=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST692,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set693=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST693,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set694=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST694,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set695=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST695,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set697=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST697,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set698=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST698,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set699=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST699,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set700=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST700,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)






test_set704=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST704,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set705=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST705,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set706=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST706,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set707=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST707,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set709=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST709,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set710=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST710,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set712=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST712,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set714=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST714,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set715=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST715,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set716=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST716,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set717=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST717,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set718=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST718,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set719=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST719,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set721=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST721,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set722=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST722,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)




test_set725=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST725,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set728=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST728,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set729=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST729,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set730=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST730,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set732=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST732,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set735=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST735,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set736=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST736,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set738=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST738,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set739=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST739,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)




test_set743=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST743,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set744=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST744,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set745=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST745,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set746=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST746,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set747=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST747,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set748=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST748,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set749=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST749,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set750=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST750,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set751=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST751,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set753=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST753,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set755=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST755,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set757=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST757,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set758=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST758,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set759=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST759,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set761=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST761,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set762=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST762,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set763=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST763,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set764=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST764,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set765=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST765,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set766=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST766,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set767=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST767,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set769=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST769,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set770=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST770,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set771=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST771,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set774=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST774,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set775=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST775,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set778=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST778,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set780=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST780,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set782=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST782,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set783=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST783,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set784=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST784,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set788=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST788,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set791=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST791,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set792=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST792,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set793=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST793,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set795=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST795,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set798=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST798,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set800=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST800,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set803=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST803,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set804=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST804,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set805=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST805,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set806=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST806,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set807=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST807,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set810=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST810,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set811=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST811,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set812=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST812,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set813=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST813,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set814=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST814,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set817=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST817,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set818=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST818,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set819=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST819,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set820=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST820,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set822=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST822,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set823=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST823,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set824=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST824,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set826=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST826,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set828=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST828,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set829=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST829,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)





test_set832=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST832,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set834=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST834,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set835=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST835,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set836=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST836,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set837=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST837,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set838=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST838,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set839=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST839,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set841=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST841,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set842=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST842,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set843=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST843,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set844=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST844,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set846=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST846,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set847=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST847,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set848=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST848,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set849=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST849,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set851=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST851,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set852=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST852,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set854=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST854,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set855=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST855,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set856=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST856,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set858=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST858,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set859=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST859,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set860=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST860,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set861=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST861,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set862=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST862,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set863=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST863,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set864=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST864,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set866=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST866,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set868=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST868,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set870=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST870,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set871=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST871,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set872=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST872,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set873=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST873,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set875=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST875,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set876=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST876,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set877=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST877,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)





test_set882=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST882,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set884=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST884,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set885=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST885,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set886=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST886,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set888=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST888,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set889=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST889,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)





test_set893=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST893,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set896=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST896,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set897=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST897,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set898=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST898,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set901=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST901,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set903=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST903,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set904=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST904,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set905=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST905,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set906=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST906,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set907=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST907,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set909=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST909,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set910=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST910,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set911=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST911,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set912=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST912,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set916=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST916,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set917=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST917,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set918=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST918,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set919=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST919,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set922=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST922,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set924=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST924,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set925=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST925,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set926=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST926,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set927=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST927,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set929=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST929,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set930=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST930,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set931=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST931,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set932=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST932,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set933=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST933,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set935=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST935,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set937=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST937,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)




test_set941=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST941,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set943=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST943,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set944=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST944,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set945=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST945,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set946=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST946,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set947=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST947,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set948=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST948,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set949=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST949,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set950=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST950,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set951=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST951,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set953=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST953,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set955=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST955,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set956=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST956,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set957=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST957,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set958=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST958,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set960=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST960,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set962=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST962,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set964=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST964,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set965=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST965,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set967=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST967,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set969=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST969,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set970=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST970,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set972=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST972,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set974=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST974,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set975=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST975,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set979=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST979,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set981=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST981,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set982=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST982,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set983=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST983,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set984=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST984,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set987=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST987,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set989=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST989,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set991=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST991,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set993=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST993,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set994=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST994,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set995=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST995,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set997=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST997,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set999=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST999,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1000=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1000,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1001=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1001,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1002=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1002,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1003=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1003,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1004=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1004,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set1006=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1006,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1009=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1009,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1011=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1011,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1012=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1012,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1013=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1013,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1014=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1014,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1015=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1015,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1016=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1016,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1018=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1018,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1020=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1020,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1022=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1022,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1023=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1023,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1025=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1025,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1026=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1026,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set1028=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1028,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1029=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1029,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1031=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1031,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1032=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1032,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1033=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1033,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)




test_set1038=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1038,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1041=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1041,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set1043=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1043,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1044=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1044,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1046=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1046,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1049=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1049,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1051=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1051,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1052=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1052,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1053=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1053,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1055=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1055,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set1057=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1057,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)





test_set1062=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1062,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1063=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1063,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1064=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1064,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1065=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1065,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1066=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1066,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1067=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1067,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1068=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1068,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1069=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1069,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1072=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1072,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1073=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1073,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1074=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1074,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1075=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1075,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1077=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1077,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1078=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1078,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1079=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1079,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1080=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1080,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1082=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1082,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1083=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1083,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1084=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1084,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1085=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1085,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1088=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1088,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1089=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1089,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1091=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1091,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1092=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1092,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1094=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1094,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1095=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1095,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set1097=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1097,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1098=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1098,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1099=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1099,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1100=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1100,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1102=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1102,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1103=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1103,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set1105=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1105,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1106=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1106,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1107=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1107,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1108=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1108,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1109=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1109,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1110=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1110,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1111=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1111,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1113=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1113,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1115=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1115,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1116=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1116,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1117=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1117,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1119=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1119,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1120=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1120,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1121=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1121,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1122=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1122,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1123=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1123,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1124=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1124,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1125=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1125,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1127=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1127,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1128=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1128,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1129=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1129,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1130=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1130,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1131=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1131,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1132=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1132,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)





test_set1135=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1135,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1136=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1136,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1137=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1137,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1138=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1138,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set1140=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1140,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1141=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1141,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1143=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1143,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1144=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1144,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1145=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1145,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1150=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1150,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1151=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1151,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1152=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1152,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1154=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1154,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1155=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1155,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1156=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1156,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1157=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1157,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1158=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1158,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1161=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1161,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1162=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1162,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)




test_set1165=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1165,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1168=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1168,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1169=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1169,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1170=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1170,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1171=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1171,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1172=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1172,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1173=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1173,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1174=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1174,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1177=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1177,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1178=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1178,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1180=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1180,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1182=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1182,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1183=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1183,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1184=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1184,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1186=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1186,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1187=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1187,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1188=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1188,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1189=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1189,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1191=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1191,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1192=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1192,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1193=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1193,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)





test_set1196=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1196,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1197=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1197,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1198=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1198,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1199=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1199,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1201=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1201,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1202=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1202,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1204=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1204,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1205=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1205,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1206=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1206,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1207=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1207,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)





test_set1212=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1212,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1214=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1214,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1215=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1215,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)





test_set1218=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1218,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1219=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1219,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1220=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1220,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1222=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1222,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1223=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1223,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1224=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1224,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1225=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1225,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1226=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1226,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1227=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1227,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1228=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1228,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)





test_set1231=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1231,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1232=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1232,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1233=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1233,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1234=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1234,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1235=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1235,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1236=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1236,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1237=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1237,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1238=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1238,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1239=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1239,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1240=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1240,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1242=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1242,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1243=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1243,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1244=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1244,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1245=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1245,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1248=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1248,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1252=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1252,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1254=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1254,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1255=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1255,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set1257=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1257,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1258=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1258,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1259=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1259,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1260=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1260,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1261=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1261,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1263=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1263,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1264=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1264,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1265=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1265,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1270=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1270,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1271=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1271,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1272=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1272,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1274=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1274,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1275=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1275,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1277=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1277,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1279=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1279,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1280=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1280,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1281=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1281,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1282=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1282,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1283=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1283,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1284=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1284,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1286=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1286,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1287=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1287,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1288=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1288,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1289=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1289,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1290=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1290,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)





test_set1295=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1295,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1296=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1296,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1297=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1297,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1298=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1298,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1300=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1300,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1302=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1302,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1304=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1304,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1305=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1305,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1306=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1306,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1307=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1307,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1308=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1308,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1315=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1315,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1316=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1316,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1318=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1318,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1319=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1319,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1321=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1321,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1322=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1322,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1323=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1323,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1324=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1324,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1325=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1325,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1326=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1326,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1327=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1327,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1328=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1328,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1330=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1330,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1333=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1333,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1334=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1334,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)





test_set1337=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1337,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1338=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1338,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1340=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1340,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1341=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1341,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1342=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1342,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1344=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1344,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1345=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1345,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1346=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1346,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1347=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1347,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1348=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1348,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1349=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1349,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1350=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1350,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1351=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1351,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1352=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1352,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1353=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1353,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1354=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1354,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1355=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1355,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1356=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1356,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1357=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1357,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1358=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1358,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1360=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1360,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1362=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1362,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1363=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1363,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1364=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1364,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1366=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1366,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1367=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1367,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1368=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1368,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1369=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1369,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1370=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1370,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1371=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1371,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1372=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1372,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1373=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1373,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1374=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1374,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set1376=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1376,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1377=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1377,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1379=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1379,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1380=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1380,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1381=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1381,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1382=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1382,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1384=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1384,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1385=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1385,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1387=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1387,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1390=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1390,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1392=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1392,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1393=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1393,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1394=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1394,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1395=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1395,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1397=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1397,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)




test_set1403=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1403,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1405=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1405,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1406=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1406,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1408=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1408,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1411=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1411,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set1413=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1413,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1414=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1414,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1416=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1416,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1417=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1417,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1418=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1418,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1419=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1419,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1420=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1420,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1421=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1421,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1422=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1422,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1423=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1423,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1424=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1424,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set1426=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1426,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)





test_set1429=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1429,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1430=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1430,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)





test_set1435=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1435,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1436=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1436,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1438=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1438,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1440=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1440,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1441=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1441,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1442=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1442,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1443=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1443,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1444=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1444,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1445=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1445,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1446=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1446,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1447=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1447,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1448=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1448,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1449=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1449,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1451=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1451,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1454=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1454,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1455=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1455,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1457=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1457,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1459=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1459,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1460=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1460,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1461=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1461,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1462=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1462,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1465=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1465,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1466=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1466,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1467=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1467,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set1469=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1469,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1472=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1472,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1474=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1474,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1475=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1475,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1476=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1476,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1477=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1477,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1480=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1480,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set1482=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1482,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1483=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1483,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1485=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1485,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1486=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1486,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set1488=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1488,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1489=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1489,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1491=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1491,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1494=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1494,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1495=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1495,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1496=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1496,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1497=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1497,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1500=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1500,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1502=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1502,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1503=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1503,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set1505=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1505,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1506=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1506,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1507=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1507,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1508=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1508,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1509=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1509,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1512=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1512,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1513=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1513,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1514=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1514,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1515=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1515,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


test_set1517=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1517,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1518=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1518,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1522=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1522,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1523=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1523,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1524=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1524,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)



test_set1526=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1526,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1527=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1527,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)

test_set1528=tf.contrib.learn.datasets.base.load_csv_with_header(
	filename=IRIS_TEST1528,
	target_dtype=np.int,
	features_dtype=np.float32,
	target_column=-1)


#c=np.zeros((36,2))
#c[np.arange(36), test_set2.target]=1

#DATA_PATH="A00001.csv", "A00002.csv"

BATCH_SIZE=100
N_FEATURES=900

def batch_generator(filenames):
	filename_queue=tf.train.string_input_producer(filenames)
	reader=tf.TextLineReader(skip_header_lines=0)
	_,value=reader.read(filename_queue)
	record_defaults=[[1.0] for _ in range(N_FEATURES)]
	record_defaults.append([1])
	content=tf.decode_csv(value, record_defaults=record_defaults)
	features=tf.stack(content[:N_FEATURES])
	label=content[-1]
	min_after_dequeue=10*BATCH_SIZE #10
	capacity=20*BATCH_SIZE          #20
	data_batch, label_batch = tf.train.shuffle_batch([features, label], batch_size=BATCH_SIZE, capacity=capacity, min_after_dequeue=min_after_dequeue)
	return data_batch, label_batch

#def tf_confusion_metrics(model, actual_classes, session, feed_dict):
#	predictions = tf.argmax(model, 1)
#	actuals = tf.argmax(actual_classes, 1)
#	ones_like_actuals = tf.ones_like(actuals)
#	zeros_like_actuals = tf.zeros_like(actuals)
#	ones_like_predictions = tf.ones_like(predictions)
#	zeros_like_predictions = tf.zeros_like(predictions)
#	tp_op = tf.reduce_sum(tf.cast(tf.logical_and(tf.equal(actuals, ones_like_actuals), tf.equal(predictions, ones_like_predictions)), "float"))
#	tn_op = tf.reduce_sum(tf.cast(tf.logical_and(tf.equal(actuals, zeros_like_actuals), tf.equal(predictions, zeros_like_predictions)), "float"))
#	fp_op = tf.reduce_sum(tf.cast(tf.logical_and(tf.equal(actuals, zeros_like_actuals), tf.equal(predictions, ones_like_predictions)), "float"))
#	fn_op = tf.reduce_sum(tf.cast(tf.logical_and(tf.equal(actuals, ones_like_actuals), tf.equal(predictions, zeros_like_predictions)), "float"))
#	tp, tn, fp, fn = session.run([tp_op, tn_op, fp_op, fn_op], feed_dict)
#	tpr = float(tp)/(float(tp) + float(fn))
#	fpr = float(fp)/(float(tp) + float(fn))
#	tnr = float(tn)/(float(tn) + float(fp))
#	#tpp = float(tp)/(float(tp) + float(fp))
#	accuracyy = (float(tp) + float(tn))/(float(tp) + float(fp) + float(fn) + float(tn))
#	recall = tpr
#	#precision = float(tp)/(float(tp) + float(fp))
#  	#f1_score = (2 * (precision * recall)) / (precision + recall)
#	#print ('Precision = ', precision)
#	print ('Recall = ', recall)
#	#print 'F1 Score = ', f1_score
#	print ('Accuracyy = ', accuracyy)
#	print ('true negative = ', tnr)
#	#print ('ppv =', tpp)


tf.set_random_seed(0.0) 

X = tf.placeholder(tf.float32, [None, 900]) 

# correct answers will go here 
Y_ = tf.placeholder(tf.float32, [None, 2]) 
# variable learning rate 
lr = tf.placeholder(tf.float32) 
# test flag for batch norm 
tst = tf.placeholder(tf.bool) 
iter = tf.placeholder(tf.int32) 
# dropout probability 
pkeep = tf.placeholder(tf.float32) 
pkeep_conv = tf.placeholder(tf.float32) 

def batchnorm(Ylogits, is_test, iteration, offset, convolutional=False): 
    exp_moving_avg = tf.train.ExponentialMovingAverage(0.999, iteration) # adding the iteration prevents from averaging across non-existing iterations 
    bnepsilon = 1e-5 
    if convolutional: 
        mean, variance = tf.nn.moments(Ylogits, [0, 1, 2]) 
    else: 
        mean, variance = tf.nn.moments(Ylogits, [0]) 
    update_moving_everages = exp_moving_avg.apply([mean, variance]) 
    m = tf.cond(is_test, lambda: exp_moving_avg.average(mean), lambda: mean) 
    v = tf.cond(is_test, lambda: exp_moving_avg.average(variance), lambda: variance) 
    Ybn = tf.nn.batch_normalization(Ylogits, m, v, offset, None, bnepsilon) 
    return Ybn, update_moving_everages 


def compatible_convolutional_noise_shape(Y): 
    noiseshape = tf.shape(Y) 
    noiseshape = noiseshape * tf.constant([1,0,0,1]) + tf.constant([0,1,1,0]) 
    return noiseshape 

K = 24  # first convolutional layer output depth 
L = 48  # second convolutional layer output depth 
M = 64  # third convolutional layer 
N = 200  # fully connected layer 
 
W1 = tf.Variable(tf.truncated_normal([6, 6, 1, K], stddev=0.1))  # 6x6 patch, 1 input channel, K output channels 
B1 = tf.Variable(tf.constant(0.1, tf.float32, [K])) 
W2 = tf.Variable(tf.truncated_normal([5, 5, K, L], stddev=0.1)) 
B2 = tf.Variable(tf.constant(0.1, tf.float32, [L])) 
W3 = tf.Variable(tf.truncated_normal([4, 4, L, M], stddev=0.1)) 
B3 = tf.Variable(tf.constant(0.1, tf.float32, [M])) 

W4 = tf.Variable(tf.truncated_normal([8 * 8 * M, N], stddev=0.1)) 
B4 = tf.Variable(tf.constant(0.1, tf.float32, [N])) 
W5 = tf.Variable(tf.truncated_normal([N, 2], stddev=0.1)) 
B5 = tf.Variable(tf.constant(0.1, tf.float32, [2])) 

X_image = tf.reshape(X, [-1, 30, 30, 1])

stride = 1  # output is 30x30 
Y1l = tf.nn.conv2d(X_image, W1, strides=[1, stride, stride, 1], padding='SAME') 
Y1bn, update_ema1 = batchnorm(Y1l, tst, iter, B1, convolutional=True) 
Y1r = tf.nn.relu(Y1bn) 
Y1 = tf.nn.dropout(Y1r, pkeep_conv, compatible_convolutional_noise_shape(Y1r)) 
stride = 2  # output is 15x15 
Y2l = tf.nn.conv2d(Y1, W2, strides=[1, stride, stride, 1], padding='SAME') 
Y2bn, update_ema2 = batchnorm(Y2l, tst, iter, B2, convolutional=True) 
Y2r = tf.nn.relu(Y2bn) 
Y2 = tf.nn.dropout(Y2r, pkeep_conv, compatible_convolutional_noise_shape(Y2r)) 
stride = 2  # output is 8x8 
Y3l = tf.nn.conv2d(Y2, W3, strides=[1, stride, stride, 1], padding='SAME') 
Y3bn, update_ema3 = batchnorm(Y3l, tst, iter, B3, convolutional=True) 
Y3r = tf.nn.relu(Y3bn) 
Y3 = tf.nn.dropout(Y3r, pkeep_conv, compatible_convolutional_noise_shape(Y3r)) 

YY = tf.reshape(Y3, shape=[-1, 8 * 8 * M])  
 
Y4l = tf.matmul(YY, W4) 
Y4bn, update_ema4 = batchnorm(Y4l, tst, iter, B4) 
Y4r = tf.nn.relu(Y4bn) 
Y4 = tf.nn.dropout(Y4r, pkeep) 
Ylogits = tf.matmul(Y4, W5) + B5 
Y = tf.nn.softmax(Ylogits) 
 
update_ema = tf.group(update_ema1, update_ema2, update_ema3, update_ema4) 

# cross-entropy loss function (= -sum(Y_i * log(Yi)) ), normalised for batches of 100  images 
# TensorFlow provides the softmax_cross_entropy_with_logits function to avoid numerical stability 
# problems with log(0) which is NaN 
cross_entropy = tf.nn.softmax_cross_entropy_with_logits(logits=Ylogits, labels=Y_) 
cross_entropy = tf.reduce_mean(cross_entropy)*100 

correct_prediction = tf.equal(tf.argmax(Y, 1), tf.argmax(Y_, 1)) 
accuracy = tf.reduce_mean(tf.cast(correct_prediction, tf.float32)) 

train_step = tf.train.AdamOptimizer(lr).minimize(cross_entropy)  
 
# init 
init = tf.global_variables_initializer() 

data_batch, label_batch = batch_generator(["A00001.csv", "A00002.csv", "A00003.csv", "A00004.csv", "A00006.csv", "A00007.csv", "A00009.csv", "A00010.csv", "A00011.csv", "A00012.csv", "A00014.csv", "A00015.csv", "A00016.csv", "A00018.csv", "A00019.csv", "A00021.csv", "A00025.csv", "A00026.csv", "A00027.csv", "A00028.csv", "A00031.csv", "A00032.csv", "A00033.csv", "A00034.csv", "A00035.csv", "A00036.csv", "A00037.csv", "A00039.csv", "A00040.csv", "A00042.csv", "A00044.csv", "A00045.csv", "A00046.csv", "A00048.csv", "A00049.csv", "A00050.csv", "A00051.csv", "A00052.csv", "A00053.csv", "A00054.csv", "A00057.csv", "A00059.csv", "A00060.csv", "A00062.csv", "A00063.csv", "A00064.csv", "A00067.csv", "A00068.csv", "A00071.csv", "A00072.csv", "A00073.csv", "A00076.csv", "A00079.csv", "A00080.csv", "A00081.csv", "A00084.csv", "A00085.csv", "A00086.csv", "A00087.csv", "A00089.csv", "A00090.csv", "A00091.csv", "A00093.csv", "A00094.csv", "A00095.csv", "A00097.csv", "A00098.csv", "A00099.csv", "A00100.csv", "A00101.csv", "A00102.csv", "A00104.csv", "A00105.csv", "A00106.csv", "A00107.csv", "A00109.csv", "A00111.csv", "A00112.csv", "A00113.csv", "A00116.csv", "A00117.csv", "A00118.csv", "A00122.csv", "A00124.csv", "A00125.csv", "A00127.csv", "A00128.csv", "A00129.csv", "A00130.csv", "A00132.csv", "A00134.csv", "A00135.csv", "A00137.csv", "A00140.csv", "A00141.csv", "A00142.csv", "A00143.csv", "A00144.csv", "A00146.csv", "A00147.csv", "A00148.csv", "A00149.csv", "A00150.csv", "A00151.csv", "A00152.csv", "A00153.csv", "A00154.csv", "A00155.csv", "A00156.csv", "A00157.csv", "A00160.csv", "A00163.csv", "A00164.csv", "A00165.csv", "A00166.csv", "A00167.csv", "A00168.csv", "A00169.csv", "A00171.csv", "A00172.csv", "A00173.csv", "A00174.csv", "A00175.csv", "A00177.csv", "A00178.csv", "A00179.csv", "A00180.csv", "A00182.csv", "A00183.csv", "A00184.csv", "A00185.csv", "A00188.csv", "A00190.csv", "A00191.csv", "A00193.csv", "A00194.csv", "A00196.csv", "A00197.csv", "A00199.csv", "A00200.csv", "A00201.csv", "A00202.csv", "A00206.csv", "A00207.csv", "A00208.csv", "A00210.csv", "A00214.csv", "A00216.csv", "A00217.csv", "A00219.csv", "A00221.csv", "A00222.csv", "A00223.csv", "A00224.csv", "A00225.csv", "A00226.csv", "A00227.csv", "A00228.csv", "A00230.csv", "A00231.csv", "A00232.csv", "A00233.csv", "A00234.csv", "A00235.csv", "A00236.csv", "A00237.csv", "A00238.csv", "A00239.csv", "A00240.csv", "A00241.csv", "A00242.csv", "A00244.csv", "A00245.csv", "A00247.csv", "A00248.csv", "A00249.csv", "A00250.csv", "A00253.csv", "A00254.csv", "A00256.csv", "A00257.csv", "A00258.csv", "A00261.csv", "A00262.csv", "A00263.csv", "A00265.csv", "A00266.csv", "A00267.csv", "A00269.csv", "A00271.csv", "A00272.csv", "A00273.csv", "A00274.csv", "A00275.csv", "A00276.csv", "A00277.csv", "A00279.csv", "A00280.csv", "A00281.csv", "A00283.csv", "A00284.csv", "A00287.csv", "A00289.csv", "A00290.csv", "A00292.csv", "A00294.csv", "A00295.csv", "A00297.csv", "A00299.csv", "A00301.csv", "A00302.csv", "A00303.csv", "A00304.csv", "A00305.csv", "A00306.csv", "A00307.csv", "A00309.csv", "A00311.csv", "A00312.csv", "A00313.csv", "A00314.csv", "A00315.csv", "A00316.csv", "A00318.csv", "A00319.csv", "A00320.csv", "A00321.csv", "A00322.csv", "A00323.csv", "A00328.csv", "A00330.csv", "A00331.csv", "A00332.csv", "A00333.csv", "A00334.csv", "A00336.csv", "A00338.csv", "A00339.csv", "A00341.csv", "A00346.csv", "A00347.csv", "A00349.csv", "A00350.csv", "A00351.csv", "A00352.csv", "A00354.csv", "A00355.csv", "A00356.csv", "A00357.csv", "A00358.csv", "A00359.csv", "A00360.csv", "A00361.csv", "A00363.csv", "A00364.csv", "A00365.csv", "A00366.csv", "A00367.csv", "A00368.csv", "A00369.csv", "A00370.csv", "A00371.csv", "A00372.csv", "A00374.csv", "A00375.csv", "A00376.csv", "A00377.csv", "A00378.csv", "A00380.csv", "A00381.csv", "A00382.csv", "A00383.csv", "A00386.csv", "A00387.csv", "A00388.csv", "A00390.csv", "A00391.csv", "A00392.csv", "A00393.csv", "A00395.csv", "A00397.csv", "A00398.csv", "A00401.csv", "A00403.csv", "A00407.csv", "A00408.csv", "A00409.csv", "A00410.csv", "A00411.csv", "A00414.csv", "A00415.csv", "A00416.csv", "A00417.csv", "A00418.csv", "A00419.csv", "A00420.csv", "A00421.csv", "A00422.csv", "A00423.csv", "A00424.csv", "A00425.csv", "A00426.csv", "A00429.csv", "A00432.csv", "A00433.csv", "A00435.csv", "A00436.csv", "A00437.csv", "A00438.csv", "A00439.csv", "A00440.csv", "A00441.csv", "A00442.csv", "A00446.csv", "A00447.csv", "A00448.csv", "A00449.csv", "A00450.csv", "A00452.csv", "A00454.csv", "A00455.csv", "A00456.csv", "A00457.csv", "A00458.csv", "A00459.csv", "A00460.csv", "A00462.csv", "A00463.csv", "A00464.csv", "A00465.csv", "A00467.csv", "A00469.csv", "A00471.csv", "A00472.csv", "A00473.csv", "A00474.csv", "A00475.csv", "A00476.csv", "A00478.csv", "A00479.csv", "A00480.csv", "A00483.csv", "A00486.csv", "A00487.csv", "A00488.csv", "A00489.csv", "A00490.csv", "A00491.csv", "A00492.csv", "A00494.csv", "A00495.csv", "A00496.csv", "A00499.csv", "A00500.csv", "A00501.csv", "A00504.csv", "A00505.csv", "A00506.csv", "A00507.csv", "A00508.csv", "A00509.csv", "A00510.csv", "A00512.csv", "A00513.csv", "A00514.csv", "A00515.csv", "A00516.csv", "A00517.csv", "A00518.csv", "A00519.csv", "A00520.csv", "A00524.csv", "A00525.csv", "A00526.csv", "A00527.csv", "A00528.csv", "A00531.csv", "A00532.csv", "A00534.csv", "A00537.csv", "A00538.csv", "A00540.csv", "A00541.csv", "A00542.csv", "A00543.csv", "A00546.csv", "A00547.csv", "A00548.csv", "A00550.csv", "A00551.csv", "A00552.csv", "A00553.csv", "A00555.csv", "A00558.csv", "A00560.csv", "A00563.csv", "A00564.csv", "A00566.csv", "A00567.csv", "A00568.csv", "A00569.csv", "A00571.csv", "A00573.csv", "A00574.csv", "A00575.csv", "A00576.csv", "A00578.csv", "A00579.csv", "A00580.csv", "A00581.csv", "A00582.csv", "A00583.csv", "A00586.csv", "A00587.csv", "A00588.csv", "A00590.csv", "A00591.csv", "A00592.csv", "A00594.csv", "A00595.csv", "A00596.csv", "A00597.csv", "A00598.csv", "A00599.csv", "A00600.csv", "A00601.csv", "A00602.csv", "A00604.csv", "A00606.csv", "A00607.csv", "A00609.csv", "A00610.csv", "A00611.csv", "A00613.csv", "A00614.csv", "A00615.csv", "A00616.csv", "A00617.csv", "A00618.csv", "A00619.csv", "A00620.csv", "A00621.csv", "A00622.csv", "A00624.csv", "A00625.csv", "A00627.csv", "A00628.csv", "A00630.csv", "A00631.csv", "A00632.csv", "A00633.csv", "A00635.csv", "A00636.csv", "A00637.csv", "A00639.csv", "A00641.csv", "A00642.csv", "A00643.csv", "A00644.csv", "A00645.csv", "A00647.csv", "A00648.csv", "A00651.csv", "A00652.csv", "A00654.csv", "A00655.csv", "A00658.csv", "A00660.csv", "A00661.csv", "A00662.csv", "A00663.csv", "A00665.csv", "A00666.csv", "A00667.csv", "A00668.csv", "A00669.csv", "A00670.csv", "A00671.csv", "A00672.csv", "A00674.csv", "A00676.csv", "A00677.csv", "A00678.csv", "A00680.csv", "A00681.csv", "A00682.csv", "A00683.csv", "A00685.csv", "A00686.csv", "A00689.csv", "A00690.csv", "A00691.csv", "A00692.csv", "A00694.csv", "A00695.csv", "A00700.csv", "A00701.csv", "A00703.csv", "A00704.csv", "A00705.csv", "A00706.csv", "A00707.csv", "A00708.csv", "A00710.csv", "A00711.csv", "A00713.csv", "A00714.csv", "A00715.csv", "A00717.csv", "A00720.csv", "A00721.csv", "A00722.csv", "A00725.csv", "A00726.csv", "A00727.csv", "A00728.csv", "A00729.csv", "A00730.csv", "A00731.csv", "A00733.csv", "A00735.csv", "A00736.csv", "A00738.csv", "A00739.csv", "A00743.csv", "A00747.csv", "A00748.csv", "A00749.csv", "A00750.csv", "A00751.csv", "A00752.csv", "A00753.csv", "A00755.csv", "A00756.csv", "A00757.csv", "A00758.csv", "A00760.csv", "A00762.csv", "A00763.csv", "A00764.csv", "A00765.csv", "A00771.csv", "A00772.csv", "A00774.csv", "A00775.csv", "A00777.csv", "A00778.csv", "A00780.csv", "A00781.csv", "A00783.csv", "A00784.csv", "A00790.csv", "A00791.csv", "A00792.csv", "A00794.csv", "A00795.csv", "A00796.csv", "A00797.csv", "A00798.csv", "A00799.csv", "A00800.csv", "A00801.csv", "A00802.csv", "A00803.csv", "A00804.csv", "A00805.csv", "A00806.csv", "A00808.csv", "A00809.csv", "A00810.csv", "A00812.csv", "A00813.csv", "A00814.csv", "A00815.csv", "A00816.csv", "A00821.csv", "A00822.csv", "A00823.csv", "A00824.csv", "A00825.csv", "A00827.csv", "A00828.csv", "A00829.csv", "A00830.csv", "A00831.csv", "A00832.csv", "A00833.csv", "A00834.csv", "A00836.csv", "A00837.csv", "A00838.csv", "A00839.csv", "A00841.csv", "A00842.csv", "A00843.csv", "A00845.csv", "A00846.csv", "A00847.csv", "A00852.csv", "A00853.csv", "A00854.csv", "A00856.csv", "A00857.csv", "A00858.csv", "A00859.csv", "A00860.csv", "A00861.csv", "A00862.csv", "A00863.csv", "A00864.csv", "A00865.csv", "A00866.csv", "A00867.csv", "A00869.csv", "A00870.csv", "A00871.csv", "A00873.csv", "A00874.csv", "A00876.csv", "A00877.csv", "A00879.csv", "A00880.csv", "A00881.csv", "A00883.csv", "A00884.csv", "A00885.csv", "A00888.csv", "A00890.csv", "A00893.csv", "A00895.csv", "A00896.csv", "A00897.csv", "A00899.csv", "A00900.csv", "A00901.csv", "A00905.csv", "A00907.csv", "A00909.csv", "A00910.csv", "A00911.csv", "A00912.csv", "A00915.csv", "A00918.csv", "A00921.csv", "A00922.csv", "A00925.csv", "A00926.csv", "A00928.csv", "A00929.csv", "A00932.csv", "A00933.csv", "A00934.csv", "A00936.csv", "A00937.csv", "A00938.csv", "A00939.csv", "A00940.csv", "A00941.csv", "A00942.csv", "A00943.csv", "A00945.csv", "A00946.csv", "A00947.csv", "A00948.csv", "A00949.csv", "A00950.csv", "A00951.csv", "A00952.csv", "A00953.csv", "A00954.csv", "A00955.csv", "A00960.csv", "A00961.csv", "A00963.csv", "A00964.csv", "A00965.csv", "A00966.csv", "A00967.csv", "A00969.csv", "A00970.csv", "A00972.csv", "A00973.csv", "A00974.csv", "A00976.csv", "A00978.csv", "A00980.csv", "A00981.csv", "A00982.csv", "A00984.csv", "A00985.csv", "A00986.csv", "A00987.csv", "A00990.csv", "A00992.csv", "A00994.csv", "A00995.csv", "A00996.csv", "A00998.csv", "A00999.csv", "A01000.csv", "A01001.csv", "A01002.csv", "A01003.csv", "A01004.csv", "A01005.csv", "A01007.csv", "A01008.csv", "A01009.csv", "A01010.csv", "A01011.csv", "A01012.csv", "A01013.csv", "A01014.csv", "A01015.csv", "A01016.csv", "A01017.csv", "A01018.csv", "A01019.csv", "A01020.csv", "A01021.csv", "A01022.csv", "A01023.csv", "A01024.csv", "A01026.csv", "A01028.csv", "A01029.csv", "A01032.csv", "A01033.csv", "A01034.csv", "A01035.csv", "A01038.csv", "A01039.csv", "A01041.csv", "A01042.csv", "A01044.csv", "A01045.csv", "A01046.csv", "A01047.csv", "A01048.csv", "A01050.csv", "A01051.csv", "A01052.csv", "A01053.csv", "A01054.csv", "A01055.csv", "A01056.csv", "A01058.csv", "A01059.csv", "A01060.csv", "A01061.csv", "A01062.csv", "A01064.csv", "A01066.csv", "A01067.csv", "A01069.csv", "A01074.csv", "A01075.csv", "A01076.csv", "A01077.csv", "A01079.csv", "A01080.csv", "A01082.csv", "A01083.csv", "A01085.csv", "A01086.csv", "A01087.csv", "A01089.csv", "A01090.csv", "A01092.csv", "A01096.csv", "A01097.csv", "A01098.csv", "A01101.csv", "A01102.csv", "A01104.csv", "A01105.csv", "A01106.csv", "A01108.csv", "A01109.csv", "A01110.csv", "A01111.csv", "A01112.csv", "A01114.csv", "A01117.csv", "A01118.csv", "A01119.csv", "A01120.csv", "A01121.csv", "A01122.csv", "A01123.csv", "A01125.csv", "A01126.csv", "A01127.csv", "A01128.csv", "A01129.csv", "A01132.csv", "A01135.csv", "A01137.csv", "A01138.csv", "A01139.csv", "A01140.csv", "A01141.csv", "A01142.csv", "A01143.csv", "A01144.csv", "A01146.csv", "A01147.csv", "A01148.csv", "A01149.csv", "A01150.csv", "A01151.csv", "A01153.csv", "A01155.csv", "A01157.csv", "A01159.csv", "A01160.csv", "A01161.csv", "A01162.csv", "A01163.csv", "A01165.csv", "A01166.csv", "A01168.csv", "A01169.csv", "A01170.csv", "A01171.csv", "A01172.csv", "A01174.csv", "A01176.csv", "A01179.csv", "A01181.csv", "A01184.csv", "A01189.csv", "A01190.csv", "A01192.csv", "A01194.csv", "A01195.csv", "A01196.csv", "A01197.csv", "A01198.csv", "A01199.csv", "A01200.csv", "A01202.csv", "A01204.csv", "A01205.csv", "A01206.csv", "A01207.csv", "A01208.csv", "A01210.csv", "A01211.csv", "A01212.csv", "A01214.csv", "A01215.csv", "A01217.csv", "A01221.csv", "A01222.csv", "A01223.csv", "A01225.csv", "A01227.csv", "A01228.csv", "A01229.csv", "A01230.csv", "A01231.csv", "A01232.csv", "A01233.csv", "A01234.csv", "A01238.csv", "A01239.csv", "A01240.csv", "A01242.csv", "A01243.csv", "A01244.csv", "A01247.csv", "A01248.csv", "A01249.csv", "A01253.csv", "A01254.csv", "A01255.csv", "A01256.csv", "A01257.csv", "A01258.csv", "A01259.csv", "A01260.csv", "A01261.csv", "A01262.csv", "A01264.csv", "A01265.csv", "A01266.csv", "A01267.csv", "A01268.csv", "A01269.csv", "A01271.csv", "A01272.csv", "A01273.csv", "A01275.csv", "A01276.csv", "A01277.csv", "A01278.csv", "A01279.csv", "A01282.csv", "A01283.csv", "A01284.csv", "A01285.csv", "A01287.csv", "A01289.csv", "A01290.csv", "A01293.csv", "A01296.csv", "A01297.csv", "A01301.csv", "A01302.csv", "A01303.csv", "A01305.csv", "A01306.csv", "A01307.csv", "A01309.csv", "A01311.csv", "A01312.csv", "A01313.csv", "A01314.csv", "A01315.csv", "A01319.csv", "A01320.csv", "A01321.csv", "A01323.csv", "A01324.csv", "A01325.csv", "A01326.csv", "A01328.csv", "A01329.csv", "A01330.csv", "A01331.csv", "A01335.csv", "A01336.csv", "A01337.csv", "A01339.csv", "A01341.csv", "A01342.csv", "A01344.csv", "A01346.csv", "A01347.csv", "A01348.csv", "A01349.csv", "A01351.csv", "A01353.csv", "A01355.csv", "A01358.csv", "A01359.csv", "A01360.csv", "A01362.csv", "A01363.csv", "A01364.csv", "A01367.csv", "A01368.csv", "A01369.csv", "A01370.csv", "A01371.csv", "A01372.csv", "A01374.csv", "A01376.csv", "A01377.csv", "A01378.csv", "A01379.csv", "A01380.csv", "A01381.csv", "A01382.csv", "A01384.csv", "A01385.csv", "A01386.csv", "A01387.csv", "A01388.csv", "A01389.csv", "A01390.csv", "A01391.csv", "A01392.csv", "A01393.csv", "A01395.csv", "A01396.csv", "A01397.csv", "A01398.csv", "A01399.csv", "A01401.csv", "A01402.csv", "A01403.csv", "A01404.csv", "A01405.csv", "A01406.csv", "A01408.csv", "A01409.csv", "A01411.csv", "A01415.csv", "A01416.csv", "A01417.csv", "A01420.csv", "A01421.csv", "A01422.csv", "A01423.csv", "A01425.csv", "A01426.csv", "A01427.csv", "A01428.csv", "A01430.csv", "A01431.csv", "A01432.csv", "A01433.csv", "A01434.csv", "A01435.csv", "A01437.csv", "A01439.csv", "A01440.csv", "A01442.csv", "A01443.csv", "A01444.csv", "A01445.csv", "A01446.csv", "A01447.csv", "A01448.csv", "A01449.csv", "A01450.csv", "A01451.csv", "A01453.csv", "A01455.csv", "A01456.csv", "A01457.csv", "A01462.csv", "A01463.csv", "A01464.csv", "A01465.csv", "A01467.csv", "A01468.csv", "A01470.csv", "A01472.csv", "A01479.csv", "A01480.csv", "A01481.csv", "A01482.csv", "A01483.csv", "A01485.csv", "A01486.csv", "A01488.csv", "A01489.csv", "A01490.csv", "A01491.csv", "A01492.csv", "A01493.csv", "A01495.csv", "A01496.csv", "A01497.csv", "A01499.csv", "A01500.csv", "A01501.csv", "A01503.csv", "A01504.csv", "A01506.csv", "A01507.csv", "A01508.csv", "A01509.csv", "A01511.csv", "A01512.csv", "A01513.csv", "A01514.csv", "A01519.csv", "A01520.csv", "A01522.csv", "A01523.csv", "A01524.csv", "A01528.csv", "A01529.csv", "A01533.csv", "A01534.csv", "A01535.csv", "A01537.csv", "A01538.csv", "A01539.csv", "A01541.csv", "A01542.csv", "A01545.csv", "A01548.csv", "A01549.csv", "A01550.csv", "A01551.csv", "A01553.csv", "A01554.csv", "A01555.csv", "A01556.csv", "A01557.csv", "A01558.csv", "A01559.csv", "A01560.csv", "A01562.csv", "A01566.csv", "A01568.csv", "A01569.csv", "A01570.csv", "A01572.csv", "A01573.csv", "A01574.csv", "A01575.csv", "A01579.csv", "A01580.csv", "A01582.csv", "A01584.csv", "A01585.csv", "A01589.csv", "A01593.csv", "A01594.csv", "A01595.csv", "A01596.csv", "A01597.csv", "A01599.csv", "A01600.csv", "A01601.csv", "A01603.csv", "A01604.csv", "A01605.csv", "A01607.csv", "A01609.csv", "A01610.csv", "A01611.csv", "A01612.csv", "A01613.csv", "A01615.csv", "A01616.csv", "A01617.csv", "A01618.csv", "A01621.csv", "A01623.csv", "A01624.csv", "A01625.csv", "A01626.csv", "A01628.csv", "A01629.csv", "A01630.csv", "A01631.csv", "A01637.csv", "A01638.csv", "A01640.csv", "A01642.csv", "A01644.csv", "A01645.csv", "A01646.csv", "A01648.csv", "A01650.csv", "A01652.csv", "A01655.csv", "A01656.csv", "A01657.csv", "A01658.csv", "A01659.csv", "A01660.csv", "A01661.csv", "A01662.csv", "A01663.csv", "A01664.csv", "A01665.csv", "A01666.csv", "A01670.csv", "A01671.csv", "A01673.csv", "A01674.csv", "A01675.csv", "A01677.csv", "A01678.csv", "A01680.csv", "A01681.csv", "A01683.csv", "A01684.csv", "A01685.csv", "A01686.csv", "A01687.csv", "A01688.csv", "A01689.csv", "A01691.csv", "A01693.csv", "A01694.csv", "A01695.csv", "A01696.csv", "A01697.csv", "A01698.csv", "A01699.csv", "A01700.csv", "A01702.csv", "A01703.csv", "A01704.csv", "A01705.csv", "A01706.csv", "A01708.csv", "A01710.csv", "A01711.csv", "A01712.csv", "A01713.csv", "A01714.csv", "A01715.csv", "A01717.csv", "A01718.csv", "A01719.csv", "A01721.csv", "A01724.csv", "A01725.csv", "A01728.csv", "A01729.csv", "A01730.csv", "A01732.csv", "A01733.csv", "A01734.csv", "A01735.csv", "A01736.csv", "A01738.csv", "A01739.csv", "A01740.csv", "A01741.csv", "A01742.csv", "A01743.csv", "A01745.csv", "A01747.csv", "A01748.csv", "A01749.csv", "A01750.csv", "A01751.csv", "A01752.csv", "A01753.csv", "A01754.csv", "A01755.csv", "A01756.csv", "A01758.csv", "A01759.csv", "A01760.csv", "A01762.csv", "A01763.csv", "A01765.csv", "A01766.csv", "A01767.csv", "A01768.csv", "A01769.csv", "A01770.csv", "A01771.csv", "A01773.csv", "A01774.csv", "A01775.csv", "A01776.csv", "A01778.csv", "A01779.csv", "A01780.csv", "A01781.csv", "A01782.csv", "A01783.csv", "A01784.csv", "A01786.csv", "A01787.csv", "A01788.csv", "A01789.csv", "A01791.csv", "A01792.csv", "A01793.csv", "A01794.csv", "A01796.csv", "A01797.csv", "A01799.csv", "A01800.csv", "A01802.csv", "A01803.csv", "A01804.csv", "A01805.csv", "A01806.csv", "A01807.csv", "A01808.csv", "A01810.csv", "A01811.csv", "A01812.csv", "A01815.csv", "A01816.csv", "A01817.csv", "A01818.csv", "A01819.csv", "A01821.csv", "A01823.csv", "A01827.csv", "A01828.csv", "A01829.csv", "A01830.csv", "A01831.csv", "A01832.csv", "A01835.csv", "A01837.csv", "A01840.csv", "A01841.csv", "A01843.csv", "A01844.csv", "A01845.csv", "A01847.csv", "A01848.csv", "A01849.csv", "A01850.csv", "A01851.csv", "A01853.csv", "A01854.csv", "A01855.csv", "A01856.csv", "A01857.csv", "A01858.csv", "A01859.csv", "A01861.csv", "A01862.csv", "A01863.csv", "A01864.csv", "A01865.csv", "A01866.csv", "A01867.csv", "A01868.csv", "A01869.csv", "A01870.csv", "A01871.csv", "A01874.csv", "A01875.csv", "A01877.csv", "A01878.csv", "A01879.csv", "A01881.csv", "A01882.csv", "A01883.csv", "A01884.csv", "A01885.csv", "A01886.csv", "A01888.csv", "A01889.csv", "A01892.csv", "A01894.csv", "A01895.csv", "A01896.csv", "A01898.csv", "A01899.csv", "A01900.csv", "A01901.csv", "A01904.csv", "A01905.csv", "A01906.csv", "A01908.csv", "A01910.csv", "A01911.csv", "A01912.csv", "A01914.csv", "A01915.csv", "A01920.csv", "A01922.csv", "A01923.csv", "A01924.csv", "A01926.csv", "A01927.csv", "A01930.csv", "A01931.csv", "A01932.csv", "A01933.csv", "A01934.csv", "A01935.csv", "A01936.csv", "A01939.csv", "A01940.csv", "A01941.csv", "A01942.csv", "A01943.csv", "A01945.csv", "A01947.csv", "A01948.csv", "A01949.csv", "A01950.csv", "A01951.csv", "A01952.csv", "A01953.csv", "A01956.csv", "A01957.csv", "A01958.csv", "A01959.csv", "A01960.csv", "A01963.csv", "A01964.csv", "A01965.csv", "A01966.csv", "A01967.csv", "A01968.csv", "A01969.csv", "A01971.csv", "A01972.csv", "A01973.csv", "A01975.csv", "A01976.csv", "A01977.csv", "A01978.csv", "A01979.csv", "A01980.csv", "A01981.csv", "A01982.csv", "A01984.csv", "A01985.csv", "A01986.csv", "A01987.csv", "A01988.csv", "A01989.csv", "A01990.csv", "A01991.csv", "A01992.csv", "A01993.csv", "A01994.csv", "A01995.csv", "A01996.csv", "A01998.csv", "A02000.csv", "A02001.csv", "A02006.csv", "A02008.csv", "A02009.csv", "A02010.csv", "A02013.csv", "A02014.csv", "A02015.csv", "A02016.csv", "A02017.csv", "A02018.csv", "A02020.csv", "A02021.csv", "A02022.csv", "A02023.csv", "A02025.csv", "A02026.csv", "A02028.csv", "A02029.csv", "A02030.csv", "A02032.csv", "A02033.csv", "A02034.csv", "A02037.csv", "A02038.csv", "A02039.csv", "A02040.csv", "A02041.csv", "A02042.csv", "A02043.csv", "A02045.csv", "A02046.csv", "A02047.csv", "A02048.csv", "A02050.csv", "A02051.csv", "A02052.csv", "A02054.csv", "A02055.csv", "A02057.csv", "A02058.csv", "A02059.csv", "A02061.csv", "A02063.csv", "A02064.csv", "A02065.csv", "A02070.csv", "A02071.csv", "A02072.csv", "A02073.csv", "A02074.csv", "A02075.csv", "A02076.csv", "A02078.csv", "A02079.csv", "A02080.csv", "A02081.csv", "A02082.csv", "A02083.csv", "A02085.csv", "A02086.csv", "A02087.csv", "A02088.csv", "A02089.csv", "A02093.csv", "A02094.csv", "A02095.csv", "A02096.csv", "A02097.csv", "A02099.csv", "A02100.csv", "A02102.csv", "A02104.csv", "A02106.csv", "A02108.csv", "A02109.csv", "A02113.csv", "A02115.csv", "A02116.csv", "A02119.csv", "A02120.csv", "A02122.csv", "A02123.csv", "A02124.csv", "A02125.csv", "A02126.csv", "A02127.csv", "A02128.csv", "A02130.csv", "A02131.csv", "A02132.csv", "A02134.csv", "A02135.csv", "A02136.csv", "A02137.csv", "A02138.csv", "A02139.csv", "A02140.csv", "A02141.csv", "A02142.csv", "A02143.csv", "A02144.csv", "A02145.csv", "A02146.csv", "A02147.csv", "A02148.csv", "A02149.csv", "A02150.csv", "A02151.csv", "A02154.csv", "A02155.csv", "A02156.csv", "A02159.csv", "A02160.csv", "A02161.csv", "A02162.csv", "A02165.csv", "A02166.csv", "A02167.csv", "A02169.csv", "A02172.csv", "A02173.csv", "A02174.csv", "A02175.csv", "A02178.csv", "A02179.csv", "A02182.csv", "A02184.csv", "A02185.csv", "A02186.csv", "A02188.csv", "A02189.csv", "A02190.csv", "A02191.csv", "A02195.csv", "A02196.csv", "A02197.csv", "A02198.csv", "A02199.csv", "A02200.csv", "A02201.csv", "A02203.csv", "A02204.csv", "A02206.csv", "A02207.csv", "A02208.csv", "A02209.csv", "A02210.csv", "A02211.csv", "A02215.csv", "A02216.csv", "A02217.csv", "A02218.csv", "A02219.csv", "A02220.csv", "A02221.csv", "A02222.csv", "A02224.csv", "A02225.csv", "A02227.csv", "A02229.csv", "A02230.csv", "A02231.csv", "A02234.csv", "A02236.csv", "A02237.csv", "A02238.csv", "A02239.csv", "A02240.csv", "A02241.csv", "A02243.csv", "A02244.csv", "A02246.csv", "A02248.csv", "A02249.csv", "A02250.csv", "A02251.csv", "A02252.csv", "A02256.csv", "A02258.csv", "A02260.csv", "A02261.csv", "A02262.csv", "A02263.csv", "A02264.csv", "A02266.csv", "A02267.csv", "A02269.csv", "A02271.csv", "A02272.csv", "A02274.csv", "A02275.csv", "A02276.csv", "A02277.csv", "A02279.csv", "A02281.csv", "A02282.csv", "A02283.csv", "A02285.csv", "A02287.csv", "A02288.csv", "A02289.csv", "A02290.csv", "A02291.csv", "A02292.csv", "A02293.csv", "A02297.csv", "A02298.csv", "A02305.csv", "A02306.csv", "A02307.csv", "A02308.csv", "A02309.csv", "A02310.csv", "A02312.csv", "A02313.csv", "A02317.csv", "A02319.csv", "A02321.csv", "A02323.csv", "A02324.csv", "A02326.csv", "A02327.csv", "A02328.csv", "A02329.csv", "A02330.csv", "A02331.csv", "A02332.csv", "A02335.csv", "A02336.csv", "A02338.csv", "A02339.csv", "A02340.csv", "A02341.csv", "A02343.csv", "A02344.csv", "A02345.csv", "A02346.csv", "A02347.csv", "A02349.csv", "A02350.csv", "A02351.csv", "A02352.csv", "A02353.csv", "A02354.csv", "A02355.csv", "A02356.csv", "A02357.csv", "A02359.csv", "A02360.csv", "A02362.csv", "A02365.csv", "A02366.csv", "A02367.csv", "A02368.csv", "A02371.csv", "A02373.csv", "A02374.csv", "A02375.csv", "A02376.csv", "A02377.csv", "A02378.csv", "A02381.csv", "A02382.csv", "A02383.csv", "A02384.csv", "A02385.csv", "A02386.csv", "A02389.csv", "A02391.csv", "A02393.csv", "A02394.csv", "A02395.csv", "A02397.csv", "A02398.csv", "A02400.csv", "A02401.csv", "A02402.csv", "A02403.csv", "A02404.csv", "A02405.csv", "A02406.csv", "A02407.csv", "A02411.csv", "A02412.csv", "A02413.csv", "A02414.csv", "A02415.csv", "A02416.csv", "A02420.csv", "A02421.csv", "A02422.csv", "A02424.csv", "A02425.csv", "A02426.csv", "A02427.csv", "A02429.csv", "A02430.csv", "A02431.csv", "A02435.csv", "A02439.csv", "A02442.csv", "A02443.csv", "A02444.csv", "A02445.csv", "A02447.csv", "A02448.csv", "A02449.csv", "A02450.csv", "A02451.csv", "A02452.csv", "A02453.csv", "A02454.csv", "A02455.csv", "A02456.csv", "A02457.csv", "A02458.csv", "A02459.csv", "A02460.csv", "A02461.csv", "A02464.csv", "A02465.csv", "A02466.csv", "A02468.csv", "A02469.csv", "A02470.csv", "A02472.csv", "A02473.csv", "A02474.csv", "A02475.csv", "A02476.csv", "A02478.csv", "A02480.csv", "A02481.csv", "A02482.csv", "A02483.csv", "A02484.csv", "A02485.csv", "A02486.csv", "A02487.csv", "A02489.csv", "A02491.csv", "A02492.csv", "A02493.csv", "A02494.csv", "A02495.csv", "A02496.csv", "A02497.csv", "A02499.csv", "A02500.csv", "A02501.csv", "A02502.csv", "A02503.csv", "A02504.csv", "A02506.csv", "A02507.csv", "A02508.csv", "A02509.csv", "A02510.csv", "A02511.csv", "A02512.csv", "A02513.csv", "A02514.csv", "A02515.csv", "A02516.csv", "A02517.csv", "A02518.csv", "A02519.csv", "A02520.csv", "A02521.csv", "A02523.csv", "A02524.csv", "A02525.csv", "A02526.csv", "A02527.csv", "A02528.csv", "A02530.csv", "A02532.csv", "A02533.csv", "A02534.csv", "A02536.csv", "A02537.csv", "A02538.csv", "A02539.csv", "A02540.csv", "A02542.csv", "A02543.csv", "A02545.csv", "A02546.csv", "A02547.csv", "A02548.csv", "A02549.csv", "A02550.csv", "A02553.csv", "A02554.csv", "A02555.csv", "A02556.csv", "A02557.csv", "A02558.csv", "A02559.csv", "A02561.csv", "A02562.csv", "A02563.csv", "A02564.csv", "A02565.csv", "A02566.csv", "A02567.csv", "A02569.csv", "A02570.csv", "A02571.csv", "A02572.csv", "A02573.csv", "A02575.csv", "A02578.csv", "A02579.csv", "A02580.csv", "A02581.csv", "A02582.csv", "A02583.csv", "A02585.csv", "A02586.csv", "A02587.csv", "A02588.csv", "A02589.csv", "A02590.csv", "A02591.csv", "A02592.csv", "A02593.csv", "A02594.csv", "A02595.csv", "A02596.csv", "A02597.csv", "A02598.csv", "A02599.csv", "A02600.csv", "A02603.csv", "A02604.csv", "A02605.csv", "A02606.csv", "A02608.csv", "A02609.csv", "A02610.csv", "A02611.csv", "A02612.csv", "A02613.csv", "A02614.csv", "A02616.csv", "A02618.csv", "A02619.csv", "A02620.csv", "A02621.csv", "A02622.csv", "A02623.csv", "A02624.csv", "A02625.csv", "A02626.csv", "A02627.csv", "A02628.csv", "A02633.csv", "A02635.csv", "A02637.csv", "A02638.csv", "A02639.csv", "A02640.csv", "A02641.csv", "A02642.csv", "A02644.csv", "A02645.csv", "A02646.csv", "A02647.csv", "A02648.csv", "A02649.csv", "A02651.csv", "A02652.csv", "A02653.csv", "A02655.csv", "A02656.csv", "A02657.csv", "A02659.csv", "A02660.csv", "A02661.csv", "A02662.csv", "A02663.csv", "A02664.csv", "A02665.csv", "A02666.csv", "A02667.csv", "A02668.csv", "A02669.csv", "A02670.csv", "A02671.csv", "A02672.csv", "A02673.csv", "A02674.csv", "A02677.csv", "A02678.csv", "A02681.csv", "A02682.csv", "A02684.csv", "A02686.csv", "A02689.csv", "A02690.csv", "A02691.csv", "A02692.csv", "A02693.csv", "A02694.csv", "A02695.csv", "A02698.csv", "A02700.csv", "A02703.csv", "A02706.csv", "A02707.csv", "A02710.csv", "A02711.csv", "A02712.csv", "A02713.csv", "A02714.csv", "A02715.csv", "A02716.csv", "A02717.csv", "A02718.csv", "A02720.csv", "A02721.csv", "A02722.csv", "A02723.csv", "A02726.csv", "A02727.csv", "A02728.csv", "A02730.csv", "A02731.csv", "A02735.csv", "A02736.csv", "A02737.csv", "A02738.csv", "A02739.csv", "A02742.csv", "A02743.csv", "A02744.csv", "A02745.csv", "A02746.csv", "A02749.csv", "A02750.csv", "A02752.csv", "A02753.csv", "A02754.csv", "A02755.csv", "A02756.csv", "A02757.csv", "A02758.csv", "A02760.csv", "A02761.csv", "A02762.csv", "A02763.csv", "A02764.csv", "A02765.csv", "A02766.csv", "A02767.csv", "A02768.csv", "A02769.csv", "A02770.csv", "A02773.csv", "A02774.csv", "A02776.csv", "A02777.csv", "A02778.csv", "A02779.csv", "A02781.csv", "A02782.csv", "A02783.csv", "A02784.csv", "A02786.csv", "A02788.csv", "A02789.csv", "A02790.csv", "A02793.csv", "A02794.csv", "A02795.csv", "A02796.csv", "A02797.csv", "A02799.csv", "A02800.csv", "A02803.csv", "A02805.csv", "A02807.csv", "A02808.csv", "A02809.csv", "A02811.csv", "A02812.csv", "A02813.csv", "A02814.csv", "A02815.csv", "A02816.csv", "A02817.csv", "A02819.csv", "A02820.csv", "A02821.csv", "A02822.csv", "A02823.csv", "A02824.csv", "A02825.csv", "A02829.csv", "A02831.csv", "A02836.csv", "A02837.csv", "A02838.csv", "A02839.csv", "A02842.csv", "A02843.csv", "A02845.csv", "A02846.csv", "A02847.csv", "A02848.csv", "A02849.csv", "A02850.csv", "A02851.csv", "A02853.csv", "A02855.csv", "A02856.csv", "A02857.csv", "A02858.csv", "A02860.csv", "A02861.csv", "A02863.csv", "A02864.csv", "A02865.csv", "A02869.csv", "A02871.csv", "A02872.csv", "A02873.csv", "A02875.csv", "A02876.csv", "A02878.csv", "A02879.csv", "A02880.csv", "A02882.csv", "A02884.csv", "A02886.csv", "A02890.csv", "A02891.csv", "A02892.csv", "A02894.csv", "A02895.csv", "A02896.csv", "A02897.csv", "A02898.csv", "A02899.csv", "A02900.csv", "A02901.csv", "A02902.csv", "A02903.csv", "A02904.csv", "A02905.csv", "A02906.csv", "A02907.csv", "A02908.csv", "A02909.csv", "A02910.csv", "A02913.csv", "A02916.csv", "A02917.csv", "A02918.csv", "A02919.csv", "A02921.csv", "A02923.csv", "A02924.csv", "A02925.csv", "A02926.csv", "A02927.csv", "A02928.csv", "A02929.csv", "A02930.csv", "A02931.csv", "A02935.csv", "A02936.csv", "A02937.csv", "A02938.csv", "A02939.csv", "A02940.csv", "A02941.csv", "A02942.csv", "A02944.csv", "A02945.csv", "A02946.csv", "A02949.csv", "A02950.csv", "A02951.csv", "A02952.csv", "A02953.csv", "A02954.csv", "A02955.csv", "A02956.csv", "A02957.csv", "A02958.csv", "A02959.csv", "A02962.csv", "A02964.csv", "A02965.csv", "A02966.csv", "A02967.csv", "A02968.csv", "A02969.csv", "A02970.csv", "A02971.csv", "A02972.csv", "A02975.csv", "A02977.csv", "A02978.csv", "A02979.csv", "A02981.csv", "A02982.csv", "A02985.csv", "A02987.csv", "A02989.csv", "A02990.csv", "A02991.csv", "A02992.csv", "A02994.csv", "A02996.csv", "A02998.csv", "A03000.csv", "A03002.csv", "A03003.csv", "A03004.csv", "A03007.csv", "A03008.csv", "A03009.csv", "A03011.csv", "A03012.csv", "A03013.csv", "A03018.csv", "A03019.csv", "A03020.csv", "A03022.csv", "A03023.csv", "A03024.csv", "A03025.csv", "A03026.csv", "A03027.csv", "A03028.csv", "A03029.csv", "A03030.csv", "A03031.csv", "A03032.csv", "A03033.csv", "A03034.csv", "A03035.csv", "A03036.csv", "A03037.csv", "A03038.csv", "A03040.csv", "A03041.csv", "A03042.csv", "A03043.csv", "A03045.csv", "A03046.csv", "A03048.csv", "A03049.csv", "A03051.csv", "A03052.csv", "A03053.csv", "A03054.csv", "A03055.csv", "A03056.csv", "A03057.csv", "A03058.csv", "A03059.csv", "A03060.csv", "A03061.csv", "A03062.csv", "A03063.csv", "A03065.csv", "A03066.csv", "A03067.csv", "A03068.csv", "A03069.csv", "A03070.csv", "A03073.csv", "A03074.csv", "A03075.csv", "A03077.csv", "A03078.csv", "A03080.csv", "A03081.csv", "A03084.csv", "A03085.csv", "A03086.csv", "A03088.csv", "A03091.csv", "A03092.csv", "A03093.csv", "A03094.csv", "A03096.csv", "A03097.csv", "A03098.csv", "A03099.csv", "A03100.csv", "A03101.csv", "A03102.csv", "A03104.csv", "A03105.csv", "A03106.csv", "A03107.csv", "A03108.csv", "A03109.csv", "A03114.csv", "A03115.csv", "A03118.csv", "A03119.csv", "A03120.csv", "A03121.csv", "A03122.csv", "A03123.csv", "A03124.csv", "A03125.csv", "A03126.csv", "A03128.csv", "A03129.csv", "A03130.csv", "A03131.csv", "A03132.csv", "A03133.csv", "A03134.csv", "A03135.csv", "A03136.csv", "A03138.csv", "A03139.csv", "A03140.csv", "A03141.csv", "A03143.csv", "A03144.csv", "A03145.csv", "A03146.csv", "A03147.csv", "A03149.csv", "A03150.csv", "A03151.csv", "A03152.csv", "A03154.csv", "A03155.csv", "A03157.csv", "A03158.csv", "A03159.csv", "A03160.csv", "A03161.csv", "A03163.csv", "A03164.csv", "A03165.csv", "A03166.csv", "A03168.csv", "A03170.csv", "A03171.csv", "A03172.csv", "A03173.csv", "A03175.csv", "A03176.csv", "A03178.csv", "A03179.csv", "A03180.csv", "A03181.csv", "A03184.csv", "A03185.csv", "A03186.csv", "A03187.csv", "A03188.csv", "A03189.csv", "A03190.csv", "A03191.csv", "A03193.csv", "A03194.csv", "A03197.csv", "A03200.csv", "A03201.csv", "A03203.csv", "A03204.csv", "A03205.csv", "A03206.csv", "A03207.csv", "A03209.csv", "A03211.csv", "A03212.csv", "A03213.csv", "A03215.csv", "A03217.csv", "A03218.csv", "A03219.csv", "A03221.csv", "A03222.csv", "A03223.csv", "A03224.csv", "A03226.csv", "A03227.csv", "A03230.csv", "A03231.csv", "A03232.csv", "A03234.csv", "A03235.csv", "A03236.csv", "A03237.csv", "A03238.csv", "A03239.csv", "A03240.csv", "A03241.csv", "A03242.csv", "A03243.csv", "A03244.csv", "A03246.csv", "A03247.csv", "A03248.csv", "A03249.csv", "A03252.csv", "A03253.csv", "A03255.csv", "A03256.csv", "A03257.csv", "A03259.csv", "A03260.csv", "A03261.csv", "A03263.csv", "A03264.csv", "A03265.csv", "A03268.csv", "A03269.csv", "A03270.csv", "A03272.csv", "A03273.csv", "A03274.csv", "A03277.csv", "A03279.csv", "A03280.csv", "A03281.csv", "A03282.csv", "A03284.csv", "A03285.csv", "A03288.csv", "A03292.csv", "A03295.csv", "A03296.csv", "A03297.csv", "A03298.csv", "A03299.csv", "A03301.csv", "A03302.csv", "A03303.csv", "A03304.csv", "A03305.csv", "A03306.csv", "A03307.csv", "A03310.csv", "A03312.csv", "A03313.csv", "A03314.csv", "A03315.csv", "A03317.csv", "A03319.csv", "A03320.csv", "A03321.csv", "A03322.csv", "A03323.csv", "A03325.csv", "A03326.csv", "A03327.csv", "A03328.csv", "A03331.csv", "A03334.csv", "A03336.csv", "A03337.csv", "A03338.csv", "A03340.csv", "A03342.csv", "A03343.csv", "A03344.csv", "A03345.csv", "A03346.csv", "A03347.csv", "A03348.csv", "A03349.csv", "A03350.csv", "A03351.csv", "A03352.csv", "A03353.csv", "A03356.csv", "A03357.csv", "A03358.csv", "A03359.csv", "A03360.csv", "A03361.csv", "A03362.csv", "A03363.csv", "A03364.csv", "A03366.csv", "A03367.csv", "A03369.csv", "A03372.csv", "A03374.csv", "A03375.csv", "A03376.csv", "A03377.csv", "A03378.csv", "A03379.csv", "A03380.csv", "A03381.csv", "A03382.csv", "A03383.csv", "A03384.csv", "A03385.csv", "A03386.csv", "A03387.csv", "A03388.csv", "A03389.csv", "A03390.csv", "A03391.csv", "A03394.csv", "A03395.csv", "A03396.csv", "A03397.csv", "A03398.csv", "A03400.csv", "A03401.csv", "A03402.csv", "A03404.csv", "A03405.csv", "A03407.csv", "A03409.csv", "A03411.csv", "A03412.csv", "A03413.csv", "A03414.csv", "A03415.csv", "A03419.csv", "A03420.csv", "A03423.csv", "A03425.csv", "A03426.csv", "A03428.csv", "A03429.csv", "A03430.csv", "A03431.csv", "A03432.csv", "A03433.csv", "A03434.csv", "A03435.csv", "A03437.csv", "A03438.csv", "A03440.csv", "A03441.csv", "A03442.csv", "A03444.csv", "A03445.csv", "A03446.csv", "A03448.csv", "A03449.csv", "A03450.csv", "A03451.csv", "A03452.csv", "A03453.csv", "A03454.csv", "A03455.csv", "A03456.csv", "A03457.csv", "A03458.csv", "A03459.csv", "A03460.csv", "A03462.csv", "A03465.csv", "A03466.csv", "A03467.csv", "A03468.csv", "A03469.csv", "A03470.csv", "A03471.csv", "A03472.csv", "A03473.csv", "A03476.csv", "A03477.csv", "A03478.csv", "A03479.csv", "A03480.csv", "A03482.csv", "A03483.csv", "A03484.csv", "A03485.csv", "A03487.csv", "A03488.csv", "A03489.csv", "A03491.csv", "A03492.csv", "A03494.csv", "A03495.csv", "A03497.csv", "A03498.csv", "A03501.csv", "A03502.csv", "A03503.csv", "A03504.csv", "A03505.csv", "A03507.csv", "A03508.csv", "A03509.csv", "A03510.csv", "A03511.csv", "A03512.csv", "A03515.csv", "A03518.csv", "A03520.csv", "A03522.csv", "A03523.csv", "A03524.csv", "A03526.csv", "A03527.csv", "A03529.csv", "A03530.csv", "A03531.csv", "A03533.csv", "A03534.csv", "A03535.csv", "A03536.csv", "A03542.csv", "A03543.csv", "A03544.csv", "A03545.csv", "A03547.csv", "A03548.csv", "A03550.csv", "A03553.csv", "A03554.csv", "A03555.csv", "A03557.csv", "A03558.csv", "A03559.csv", "A03560.csv", "A03561.csv", "A03562.csv", "A03563.csv", "A03564.csv", "A03565.csv", "A03566.csv", "A03567.csv", "A03568.csv", "A03569.csv", "A03570.csv", "A03572.csv", "A03573.csv", "A03574.csv", "A03576.csv", "A03580.csv", "A03581.csv", "A03584.csv", "A03585.csv", "A03586.csv", "A03587.csv", "A03588.csv", "A03589.csv", "A03590.csv", "A03592.csv", "A03593.csv", "A03594.csv", "A03595.csv", "A03596.csv", "A03599.csv", "A03600.csv", "A03602.csv", "A03603.csv", "A03604.csv", "A03605.csv", "A03606.csv", "A03607.csv", "A03608.csv", "A03610.csv", "A03611.csv", "A03613.csv", "A03617.csv", "A03618.csv", "A03622.csv", "A03623.csv", "A03625.csv", "A03626.csv", "A03627.csv", "A03628.csv", "A03629.csv", "A03631.csv", "A03632.csv", "A03634.csv", "A03635.csv", "A03636.csv", "A03637.csv", "A03638.csv", "A03639.csv", "A03641.csv", "A03642.csv", "A03644.csv", "A03645.csv", "A03647.csv", "A03648.csv", "A03649.csv", "A03650.csv", "A03651.csv", "A03652.csv", "A03654.csv", "A03655.csv", "A03656.csv", "A03657.csv", "A03658.csv", "A03660.csv", "A03662.csv", "A03663.csv", "A03666.csv", "A03668.csv", "A03670.csv", "A03671.csv", "A03672.csv", "A03673.csv", "A03674.csv", "A03675.csv", "A03676.csv", "A03677.csv", "A03678.csv", "A03679.csv", "A03680.csv", "A03681.csv", "A03682.csv", "A03684.csv", "A03685.csv", "A03686.csv", "A03688.csv", "A03689.csv", "A03690.csv", "A03691.csv", "A03693.csv", "A03695.csv", "A03697.csv", "A03698.csv", "A03699.csv", "A03700.csv", "A03702.csv", "A03703.csv", "A03704.csv", "A03706.csv", "A03707.csv", "A03709.csv", "A03710.csv", "A03711.csv", "A03712.csv", "A03713.csv", "A03715.csv", "A03716.csv", "A03718.csv", "A03720.csv", "A03722.csv", "A03726.csv", "A03728.csv", "A03729.csv", "A03731.csv", "A03733.csv", "A03734.csv", "A03735.csv", "A03737.csv", "A03739.csv", "A03741.csv", "A03743.csv", "A03744.csv", "A03745.csv", "A03746.csv", "A03747.csv", "A03748.csv", "A03749.csv", "A03750.csv", "A03751.csv", "A03753.csv", "A03754.csv", "A03755.csv", "A03759.csv", "A03760.csv", "A03761.csv", "A03762.csv", "A03764.csv", "A03765.csv", "A03767.csv", "A03768.csv", "A03769.csv", "A03770.csv", "A03772.csv", "A03774.csv", "A03776.csv", "A03777.csv", "A03779.csv", "A03782.csv", "A03783.csv", "A03784.csv", "A03785.csv", "A03786.csv", "A03787.csv", "A03788.csv", "A03790.csv", "A03791.csv", "A03792.csv", "A03795.csv", "A03796.csv", "A03799.csv", "A03800.csv", "A03801.csv", "A03803.csv", "A03804.csv", "A03806.csv", "A03809.csv", "A03811.csv", "A03813.csv", "A03815.csv", "A03818.csv", "A03819.csv", "A03821.csv", "A03823.csv", "A03824.csv", "A03825.csv", "A03827.csv", "A03832.csv", "A03834.csv", "A03835.csv", "A03836.csv", "A03838.csv", "A03839.csv", "A03840.csv", "A03841.csv", "A03843.csv", "A03844.csv", "A03845.csv", "A03850.csv", "A03853.csv", "A03854.csv", "A03855.csv", "A03856.csv", "A03857.csv", "A03858.csv", "A03859.csv", "A03860.csv", "A03863.csv", "A03864.csv", "A03865.csv", "A03866.csv", "A03867.csv", "A03868.csv", "A03871.csv", "A03873.csv", "A03874.csv", "A03875.csv", "A03876.csv", "A03877.csv", "A03878.csv", "A03881.csv", "A03882.csv", "A03883.csv", "A03884.csv", "A03885.csv", "A03886.csv", "A03887.csv", "A03888.csv", "A03889.csv", "A03891.csv", "A03892.csv", "A03893.csv", "A03894.csv", "A03895.csv", "A03896.csv", "A03897.csv", "A03899.csv", "A03900.csv", "A03901.csv", "A03902.csv", "A03903.csv", "A03905.csv", "A03906.csv", "A03907.csv", "A03908.csv", "A03909.csv", "A03910.csv", "A03911.csv", "A03912.csv", "A03915.csv", "A03916.csv", "A03917.csv", "A03918.csv", "A03921.csv", "A03922.csv", "A03923.csv", "A03925.csv", "A03926.csv", "A03927.csv", "A03928.csv", "A03929.csv", "A03930.csv", "A03932.csv", "A03933.csv", "A03939.csv", "A03940.csv", "A03941.csv", "A03942.csv", "A03943.csv", "A03945.csv", "A03946.csv", "A03948.csv", "A03949.csv", "A03950.csv", "A03951.csv", "A03952.csv", "A03953.csv", "A03954.csv", "A03955.csv", "A03956.csv", "A03957.csv", "A03958.csv", "A03960.csv", "A03961.csv", "A03962.csv", "A03963.csv", "A03964.csv", "A03966.csv", "A03967.csv", "A03968.csv", "A03971.csv", "A03972.csv", "A03973.csv", "A03974.csv", "A03975.csv", "A03978.csv", "A03979.csv", "A03981.csv", "A03982.csv", "A03983.csv", "A03984.csv", "A03985.csv", "A03987.csv", "A03988.csv", "A03989.csv", "A03990.csv", "A03991.csv", "A03992.csv", "A03993.csv", "A03995.csv", "A03997.csv", "A03998.csv", "A04000.csv", "A04004.csv", "A04006.csv", "A04007.csv", "A04008.csv", "A04009.csv", "A04010.csv", "A04011.csv", "A04012.csv", "A04015.csv", "A04017.csv", "A04019.csv", "A04020.csv", "A04022.csv", "A04023.csv", "A04024.csv", "A04025.csv", "A04026.csv", "A04027.csv", "A04028.csv", "A04030.csv", "A04032.csv", "A04033.csv", "A04034.csv", "A04035.csv", "A04036.csv", "A04037.csv", "A04040.csv", "A04041.csv", "A04042.csv", "A04043.csv", "A04044.csv", "A04045.csv", "A04046.csv", "A04048.csv", "A04050.csv", "A04051.csv", "A04053.csv", "A04054.csv", "A04056.csv", "A04058.csv", "A04059.csv", "A04060.csv", "A04061.csv", "A04064.csv", "A04065.csv", "A04066.csv", "A04067.csv", "A04068.csv", "A04069.csv", "A04070.csv", "A04071.csv", "A04072.csv", "A04073.csv", "A04075.csv", "A04076.csv", "A04077.csv", "A04079.csv", "A04080.csv", "A04083.csv", "A04084.csv", "A04087.csv", "A04088.csv", "A04089.csv", "A04090.csv", "A04091.csv", "A04093.csv", "A04094.csv", "A04095.csv", "A04097.csv", "A04099.csv", "A04100.csv", "A04101.csv", "A04102.csv", "A04105.csv", "A04106.csv", "A04107.csv", "A04111.csv", "A04112.csv", "A04114.csv", "A04115.csv", "A04116.csv", "A04117.csv", "A04118.csv", "A04119.csv", "A04120.csv", "A04121.csv", "A04122.csv", "A04123.csv", "A04124.csv", "A04125.csv", "A04126.csv", "A04127.csv", "A04128.csv", "A04131.csv", "A04132.csv", "A04133.csv", "A04134.csv", "A04136.csv", "A04138.csv", "A04139.csv", "A04140.csv", "A04141.csv", "A04142.csv", "A04143.csv", "A04144.csv", "A04145.csv", "A04146.csv", "A04147.csv", "A04148.csv", "A04151.csv", "A04153.csv", "A04154.csv", "A04155.csv", "A04156.csv", "A04157.csv", "A04158.csv", "A04160.csv", "A04161.csv", "A04162.csv", "A04163.csv", "A04165.csv", "A04166.csv", "A04169.csv", "A04171.csv", "A04172.csv", "A04178.csv", "A04179.csv", "A04180.csv", "A04181.csv", "A04182.csv", "A04187.csv", "A04188.csv", "A04189.csv", "A04190.csv", "A04191.csv", "A04192.csv", "A04193.csv", "A04194.csv", "A04197.csv", "A04199.csv", "A04202.csv", "A04203.csv", "A04204.csv", "A04205.csv", "A04206.csv", "A04207.csv", "A04208.csv", "A04210.csv", "A04211.csv", "A04212.csv", "A04213.csv", "A04217.csv", "A04218.csv", "A04219.csv", "A04220.csv", "A04221.csv", "A04223.csv", "A04224.csv", "A04225.csv", "A04226.csv", "A04229.csv", "A04233.csv", "A04234.csv", "A04235.csv", "A04236.csv", "A04237.csv", "A04239.csv", "A04243.csv", "A04245.csv", "A04246.csv", "A04247.csv", "A04248.csv", "A04253.csv", "A04255.csv", "A04256.csv", "A04257.csv", "A04260.csv", "A04261.csv", "A04262.csv", "A04263.csv", "A04265.csv", "A04267.csv", "A04269.csv", "A04270.csv", "A04272.csv", "A04273.csv", "A04275.csv", "A04276.csv", "A04277.csv", "A04278.csv", "A04280.csv", "A04281.csv", "A04283.csv", "A04285.csv", "A04287.csv", "A04289.csv", "A04291.csv", "A04292.csv", "A04294.csv", "A04295.csv", "A04298.csv", "A04299.csv", "A04300.csv", "A04301.csv", "A04302.csv", "A04304.csv", "A04305.csv", "A04306.csv", "A04307.csv", "A04311.csv", "A04312.csv", "A04313.csv", "A04314.csv", "A04317.csv", "A04319.csv", "A04321.csv", "A04323.csv", "A04325.csv", "A04326.csv", "A04327.csv", "A04328.csv", "A04329.csv", "A04330.csv", "A04332.csv", "A04333.csv", "A04334.csv", "A04336.csv", "A04337.csv", "A04338.csv", "A04339.csv", "A04340.csv", "A04341.csv", "A04342.csv", "A04343.csv", "A04344.csv", "A04347.csv", "A04348.csv", "A04349.csv", "A04350.csv", "A04351.csv", "A04352.csv", "A04353.csv", "A04354.csv", "A04355.csv", "A04358.csv", "A04359.csv", "A04364.csv", "A04366.csv", "A04367.csv", "A04368.csv", "A04371.csv", "A04373.csv", "A04375.csv", "A04376.csv", "A04377.csv", "A04378.csv", "A04379.csv", "A04380.csv", "A04381.csv", "A04382.csv", "A04383.csv", "A04385.csv", "A04387.csv", "A04388.csv", "A04389.csv", "A04390.csv", "A04391.csv", "A04392.csv", "A04393.csv", "A04394.csv", "A04395.csv", "A04396.csv", "A04397.csv", "A04398.csv", "A04399.csv", "A04401.csv", "A04402.csv", "A04403.csv", "A04404.csv", "A04405.csv", "A04406.csv", "A04408.csv", "A04409.csv", "A04410.csv", "A04411.csv", "A04412.csv", "A04413.csv", "A04414.csv", "A04419.csv", "A04420.csv", "A04422.csv", "A04423.csv", "A04424.csv", "A04425.csv", "A04426.csv", "A04430.csv", "A04431.csv", "A04432.csv", "A04434.csv", "A04436.csv", "A04437.csv", "A04438.csv", "A04439.csv", "A04442.csv", "A04444.csv", "A04445.csv", "A04446.csv", "A04447.csv", "A04448.csv", "A04449.csv", "A04450.csv", "A04453.csv", "A04454.csv", "A04455.csv", "A04456.csv", "A04457.csv", "A04459.csv", "A04461.csv", "A04462.csv", "A04464.csv", "A04467.csv", "A04468.csv", "A04472.csv", "A04473.csv", "A04474.csv", "A04475.csv", "A04477.csv", "A04478.csv", "A04479.csv", "A04480.csv", "A04481.csv", "A04482.csv", "A04483.csv", "A04484.csv", "A04485.csv", "A04486.csv", "A04487.csv", "A04488.csv", "A04489.csv", "A04490.csv", "A04492.csv", "A04493.csv", "A04497.csv", "A04498.csv", "A04499.csv", "A04500.csv", "A04502.csv", "A04504.csv", "A04505.csv", "A04506.csv", "A04507.csv", "A04508.csv", "A04510.csv", "A04511.csv", "A04513.csv", "A04515.csv", "A04516.csv", "A04517.csv", "A04518.csv", "A04523.csv", "A04525.csv", "A04526.csv", "A04528.csv", "A04530.csv", "A04532.csv", "A04534.csv", "A04535.csv", "A04536.csv", "A04537.csv", "A04538.csv", "A04540.csv", "A04542.csv", "A04543.csv", "A04546.csv", "A04547.csv", "A04548.csv", "A04549.csv", "A04551.csv", "A04552.csv", "A04553.csv", "A04554.csv", "A04556.csv", "A04558.csv", "A04559.csv", "A04560.csv", "A04561.csv", "A04563.csv", "A04564.csv", "A04565.csv", "A04567.csv", "A04570.csv", "A04572.csv", "A04573.csv", "A04577.csv", "A04578.csv", "A04579.csv", "A04580.csv", "A04582.csv", "A04583.csv", "A04585.csv", "A04587.csv", "A04589.csv", "A04590.csv", "A04591.csv", "A04593.csv", "A04594.csv", "A04595.csv", "A04596.csv", "A04598.csv", "A04599.csv", "A04601.csv", "A04602.csv", "A04603.csv", "A04604.csv", "A04606.csv", "A04608.csv", "A04609.csv", "A04610.csv", "A04611.csv", "A04612.csv", "A04613.csv", "A04614.csv", "A04615.csv", "A04616.csv", "A04617.csv", "A04618.csv", "A04619.csv", "A04620.csv", "A04622.csv", "A04624.csv", "A04625.csv", "A04626.csv", "A04627.csv", "A04628.csv", "A04629.csv", "A04631.csv", "A04632.csv", "A04633.csv", "A04634.csv", "A04636.csv", "A04637.csv", "A04639.csv", "A04640.csv", "A04642.csv", "A04645.csv", "A04646.csv", "A04647.csv", "A04648.csv", "A04649.csv", "A04650.csv", "A04651.csv", "A04654.csv", "A04655.csv", "A04656.csv", "A04657.csv", "A04658.csv", "A04659.csv", "A04660.csv", "A04662.csv", "A04664.csv", "A04666.csv", "A04668.csv", "A04669.csv", "A04670.csv", "A04671.csv", "A04672.csv", "A04673.csv", "A04675.csv", "A04676.csv", "A04677.csv", "A04680.csv", "A04681.csv", "A04683.csv", "A04684.csv", "A04686.csv", "A04687.csv", "A04688.csv", "A04689.csv", "A04690.csv", "A04691.csv", "A04692.csv", "A04694.csv", "A04695.csv", "A04696.csv", "A04697.csv", "A04698.csv", "A04699.csv", "A04700.csv", "A04703.csv", "A04704.csv", "A04705.csv", "A04706.csv", "A04707.csv", "A04708.csv", "A04709.csv", "A04711.csv", "A04712.csv", "A04713.csv", "A04714.csv", "A04716.csv", "A04717.csv", "A04718.csv", "A04721.csv", "A04724.csv", "A04725.csv", "A04726.csv", "A04727.csv", "A04728.csv", "A04730.csv", "A04731.csv", "A04733.csv", "A04739.csv", "A04740.csv", "A04743.csv", "A04744.csv", "A04746.csv", "A04747.csv", "A04748.csv", "A04749.csv", "A04751.csv", "A04752.csv", "A04754.csv", "A04755.csv", "A04757.csv", "A04758.csv", "A04759.csv", "A04760.csv", "A04762.csv", "A04764.csv", "A04765.csv", "A04766.csv", "A04767.csv", "A04768.csv", "A04770.csv", "A04771.csv", "A04772.csv", "A04773.csv", "A04774.csv", "A04775.csv", "A04776.csv", "A04777.csv", "A04778.csv", "A04779.csv", "A04781.csv", "A04782.csv", "A04784.csv", "A04785.csv", "A04786.csv", "A04787.csv", "A04788.csv", "A04789.csv", "A04790.csv", "A04791.csv", "A04792.csv", "A04793.csv", "A04794.csv", "A04795.csv", "A04798.csv", "A04799.csv", "A04800.csv", "A04801.csv", "A04802.csv", "A04804.csv", "A04806.csv", "A04807.csv", "A04808.csv", "A04810.csv", "A04811.csv", "A04813.csv", "A04814.csv", "A04815.csv", "A04816.csv", "A04817.csv", "A04818.csv", "A04819.csv", "A04821.csv", "A04823.csv", "A04824.csv", "A04826.csv", "A04827.csv", "A04831.csv", "A04833.csv", "A04834.csv", "A04837.csv", "A04839.csv", "A04841.csv", "A04842.csv", "A04843.csv", "A04845.csv", "A04847.csv", "A04848.csv", "A04849.csv", "A04850.csv", "A04851.csv", "A04854.csv", "A04855.csv", "A04856.csv", "A04857.csv", "A04858.csv", "A04859.csv", "A04860.csv", "A04861.csv", "A04863.csv", "A04864.csv", "A04866.csv", "A04868.csv", "A04870.csv", "A04871.csv", "A04876.csv", "A04878.csv", "A04879.csv", "A04880.csv", "A04881.csv", "A04882.csv", "A04883.csv", "A04884.csv", "A04885.csv", "A04886.csv", "A04887.csv", "A04890.csv", "A04891.csv", "A04894.csv", "A04896.csv", "A04898.csv", "A04899.csv", "A04900.csv", "A04901.csv", "A04902.csv", "A04903.csv", "A04905.csv", "A04906.csv", "A04907.csv", "A04908.csv", "A04910.csv", "A04911.csv", "A04917.csv", "A04919.csv", "A04920.csv", "A04921.csv", "A04922.csv", "A04923.csv", "A04924.csv", "A04925.csv", "A04926.csv", "A04928.csv", "A04929.csv", "A04930.csv", "A04932.csv", "A04934.csv", "A04935.csv", "A04936.csv", "A04937.csv", "A04938.csv", "A04940.csv", "A04941.csv", "A04942.csv", "A04943.csv", "A04945.csv", "A04946.csv", "A04947.csv", "A04949.csv", "A04950.csv", "A04952.csv", "A04953.csv", "A04954.csv", "A04956.csv", "A04957.csv", "A04958.csv", "A04959.csv", "A04961.csv", "A04963.csv", "A04964.csv", "A04965.csv", "A04967.csv", "A04968.csv", "A04969.csv", "A04972.csv", "A04974.csv", "A04975.csv", "A04978.csv", "A04979.csv", "A04983.csv", "A04984.csv", "A04985.csv", "A04987.csv", "A04988.csv", "A04990.csv", "A04991.csv", "A04992.csv", "A04993.csv", "A04994.csv", "A04995.csv", "A04996.csv", "A04997.csv", "A05000.csv", "A05001.csv", "A05002.csv", "A05003.csv", "A05005.csv", "A05006.csv", "A05007.csv", "A05008.csv", "A05009.csv", "A05011.csv", "A05013.csv", "A05014.csv", "A05021.csv", "A05022.csv", "A05023.csv", "A05024.csv", "A05025.csv", "A05028.csv", "A05031.csv", "A05033.csv", "A05034.csv", "A05035.csv", "A05036.csv", "A05038.csv", "A05040.csv", "A05041.csv", "A05042.csv", "A05043.csv", "A05048.csv", "A05049.csv", "A05051.csv", "A05052.csv", "A05053.csv", "A05055.csv", "A05057.csv", "A05058.csv", "A05059.csv", "A05061.csv", "A05062.csv", "A05065.csv", "A05069.csv", "A05071.csv", "A05073.csv", "A05074.csv", "A05075.csv", "A05077.csv", "A05078.csv", "A05080.csv", "A05081.csv", "A05082.csv", "A05083.csv", "A05084.csv", "A05085.csv", "A05087.csv", "A05088.csv", "A05089.csv", "A05091.csv", "A05092.csv", "A05094.csv", "A05095.csv", "A05097.csv", "A05101.csv", "A05102.csv", "A05104.csv", "A05105.csv", "A05106.csv", "A05107.csv", "A05109.csv", "A05110.csv", "A05111.csv", "A05112.csv", "A05114.csv", "A05115.csv", "A05116.csv", "A05117.csv", "A05118.csv", "A05119.csv", "A05120.csv", "A05121.csv", "A05122.csv", "A05124.csv", "A05126.csv", "A05127.csv", "A05128.csv", "A05130.csv", "A05131.csv", "A05133.csv", "A05134.csv", "A05136.csv", "A05137.csv", "A05138.csv", "A05140.csv", "A05141.csv", "A05142.csv", "A05143.csv", "A05145.csv", "A05146.csv", "A05148.csv", "A05149.csv", "A05151.csv", "A05152.csv", "A05154.csv", "A05155.csv", "A05156.csv", "A05157.csv", "A05158.csv", "A05159.csv", "A05161.csv", "A05162.csv", "A05164.csv", "A05165.csv", "A05168.csv", "A05169.csv", "A05172.csv", "A05173.csv", "A05174.csv", "A05177.csv", "A05179.csv", "A05182.csv", "A05183.csv", "A05184.csv", "A05185.csv", "A05187.csv", "A05188.csv", "A05189.csv", "A05190.csv", "A05191.csv", "A05192.csv", "A05193.csv", "A05194.csv", "A05195.csv", "A05196.csv", "A05198.csv", "A05199.csv", "A05200.csv", "A05202.csv", "A05203.csv", "A05204.csv", "A05205.csv", "A05209.csv", "A05210.csv", "A05212.csv", "A05215.csv", "A05218.csv", "A05219.csv", "A05221.csv", "A05222.csv", "A05223.csv", "A05225.csv", "A05226.csv", "A05227.csv", "A05228.csv", "A05229.csv", "A05230.csv", "A05231.csv", "A05233.csv", "A05235.csv", "A05236.csv", "A05237.csv", "A05238.csv", "A05239.csv", "A05240.csv", "A05245.csv", "A05246.csv", "A05248.csv", "A05249.csv", "A05250.csv", "A05251.csv", "A05253.csv", "A05254.csv", "A05255.csv", "A05257.csv", "A05259.csv", "A05260.csv", "A05261.csv", "A05262.csv", "A05263.csv", "A05264.csv", "A05265.csv", "A05267.csv", "A05268.csv", "A05270.csv", "A05271.csv", "A05272.csv", "A05273.csv", "A05275.csv", "A05278.csv", "A05279.csv", "A05281.csv", "A05284.csv", "A05286.csv", "A05287.csv", "A05288.csv", "A05289.csv", "A05290.csv", "A05291.csv", "A05292.csv", "A05293.csv", "A05294.csv", "A05295.csv", "A05296.csv", "A05298.csv", "A05299.csv", "A05303.csv", "A05304.csv", "A05307.csv", "A05313.csv", "A05314.csv", "A05315.csv", "A05317.csv", "A05318.csv", "A05320.csv", "A05321.csv", "A05322.csv", "A05323.csv", "A05324.csv", "A05326.csv", "A05328.csv", "A05330.csv", "A05333.csv", "A05334.csv", "A05335.csv", "A05337.csv", "A05339.csv", "A05341.csv", "A05342.csv", "A05344.csv", "A05345.csv", "A05346.csv", "A05347.csv", "A05348.csv", "A05349.csv", "A05353.csv", "A05354.csv", "A05357.csv", "A05358.csv", "A05361.csv", "A05363.csv", "A05366.csv", "A05368.csv", "A05369.csv", "A05370.csv", "A05371.csv", "A05372.csv", "A05374.csv", "A05375.csv", "A05377.csv", "A05378.csv", "A05380.csv", "A05382.csv", "A05384.csv", "A05385.csv", "A05386.csv", "A05387.csv", "A05388.csv", "A05389.csv", "A05391.csv", "A05392.csv", "A05394.csv", "A05395.csv", "A05396.csv", "A05397.csv", "A05399.csv", "A05402.csv", "A05403.csv", "A05404.csv", "A05405.csv", "A05406.csv", "A05407.csv", "A05408.csv", "A05409.csv", "A05410.csv", "A05411.csv", "A05412.csv", "A05413.csv", "A05414.csv", "A05416.csv", "A05417.csv", "A05418.csv", "A05421.csv", "A05422.csv", "A05423.csv", "A05424.csv", "A05426.csv", "A05427.csv", "A05429.csv", "A05430.csv", "A05431.csv", "A05432.csv", "A05433.csv", "A05438.csv", "A05439.csv", "A05440.csv", "A05441.csv", "A05445.csv", "A05446.csv", "A05447.csv", "A05449.csv", "A05450.csv", "A05451.csv", "A05452.csv", "A05455.csv", "A05456.csv", "A05457.csv", "A05458.csv", "A05459.csv", "A05460.csv", "A05461.csv", "A05463.csv", "A05465.csv", "A05466.csv", "A05467.csv", "A05468.csv", "A05469.csv", "A05470.csv", "A05472.csv", "A05473.csv", "A05474.csv", "A05475.csv", "A05476.csv", "A05477.csv", "A05478.csv", "A05479.csv", "A05480.csv", "A05482.csv", "A05486.csv", "A05487.csv", "A05488.csv", "A05490.csv", "A05491.csv", "A05493.csv", "A05495.csv", "A05496.csv", "A05497.csv", "A05498.csv", "A05499.csv", "A05500.csv", "A05501.csv", "A05504.csv", "A05505.csv", "A05506.csv", "A05507.csv", "A05508.csv", "A05510.csv", "A05511.csv", "A05512.csv", "A05513.csv", "A05515.csv", "A05516.csv", "A05518.csv", "A05519.csv", "A05521.csv", "A05524.csv", "A05525.csv", "A05526.csv", "A05529.csv", "A05530.csv", "A05531.csv", "A05532.csv", "A05533.csv", "A05534.csv", "A05535.csv", "A05536.csv", "A05537.csv", "A05538.csv", "A05541.csv", "A05543.csv", "A05544.csv", "A05545.csv", "A05547.csv", "A05548.csv", "A05550.csv", "A05552.csv", "A05553.csv", "A05554.csv", "A05555.csv", "A05559.csv", "A05560.csv", "A05561.csv", "A05562.csv", "A05563.csv", "A05564.csv", "A05565.csv", "A05566.csv", "A05567.csv", "A05569.csv", "A05570.csv", "A05572.csv", "A05573.csv", "A05574.csv", "A05575.csv", "A05576.csv", "A05577.csv", "A05579.csv", "A05580.csv", "A05581.csv", "A05582.csv", "A05583.csv", "A05584.csv", "A05588.csv", "A05595.csv", "A05596.csv", "A05601.csv", "A05602.csv", "A05604.csv", "A05605.csv", "A05606.csv", "A05607.csv", "A05610.csv", "A05611.csv", "A05612.csv", "A05613.csv", "A05615.csv", "A05617.csv", "A05621.csv", "A05622.csv", "A05623.csv", "A05625.csv", "A05629.csv", "A05633.csv", "A05634.csv", "A05635.csv", "A05636.csv", "A05641.csv", "A05642.csv", "A05645.csv", "A05646.csv", "A05647.csv", "A05649.csv", "A05650.csv", "A05651.csv", "A05652.csv", "A05656.csv", "A05657.csv", "A05658.csv", "A05660.csv", "A05661.csv", "A05662.csv", "A05664.csv", "A05666.csv", "A05669.csv", "A05671.csv", "A05672.csv", "A05673.csv", "A05675.csv", "A05676.csv", "A05677.csv", "A05678.csv", "A05681.csv", "A05682.csv", "A05687.csv", "A05688.csv", "A05690.csv", "A05691.csv", "A05692.csv", "A05697.csv", "A05698.csv", "A05699.csv", "A05700.csv", "A05701.csv", "A05702.csv", "A05704.csv", "A05705.csv", "A05706.csv", "A05709.csv", "A05710.csv", "A05711.csv", "A05713.csv", "A05716.csv", "A05717.csv", "A05718.csv", "A05719.csv", "A05721.csv", "A05722.csv", "A05724.csv", "A05725.csv", "A05727.csv", "A05728.csv", "A05731.csv", "A05733.csv", "A05736.csv", "A05737.csv", "A05738.csv", "A05739.csv", "A05740.csv", "A05742.csv", "A05743.csv", "A05744.csv", "A05745.csv", "A05747.csv", "A05748.csv", "A05751.csv", "A05752.csv", "A05753.csv", "A05754.csv", "A05755.csv", "A05756.csv", "A05757.csv", "A05759.csv", "A05761.csv", "A05762.csv", "A05763.csv", "A05769.csv", "A05770.csv", "A05772.csv", "A05773.csv", "A05777.csv", "A05779.csv", "A05780.csv", "A05781.csv", "A05784.csv", "A05785.csv", "A05786.csv", "A05790.csv", "A05791.csv", "A05792.csv", "A05793.csv", "A05794.csv", "A05795.csv", "A05797.csv", "A05799.csv", "A05800.csv", "A05802.csv", "A05803.csv", "A05805.csv", "A05806.csv", "A05808.csv", "A05809.csv", "A05810.csv", "A05811.csv", "A05812.csv", "A05813.csv", "A05814.csv", "A05815.csv", "A05816.csv", "A05820.csv", "A05821.csv", "A05824.csv", "A05826.csv", "A05827.csv", "A05828.csv", "A05830.csv", "A05833.csv", "A05834.csv", "A05835.csv", "A05836.csv", "A05837.csv", "A05839.csv", "A05843.csv", "A05844.csv", "A05847.csv", "A05849.csv", "A05851.csv", "A05852.csv", "A05853.csv", "A05854.csv", "A05855.csv", "A05856.csv", "A05858.csv", "A05859.csv", "A05860.csv", "A05861.csv", "A05862.csv", "A05863.csv", "A05865.csv", "A05866.csv", "A05868.csv", "A05872.csv", "A05873.csv", "A05875.csv", "A05876.csv", "A05877.csv", "A05878.csv", "A05879.csv", "A05880.csv", "A05883.csv", "A05885.csv", "A05887.csv", "A05888.csv", "A05890.csv", "A05891.csv", "A05892.csv", "A05893.csv", "A05894.csv", "A05897.csv", "A05898.csv", "A05899.csv", "A05903.csv", "A05904.csv", "A05905.csv", "A05906.csv", "A05908.csv", "A05910.csv", "A05912.csv", "A05914.csv", "A05915.csv", "A05918.csv", "A05919.csv", "A05920.csv", "A05926.csv", "A05928.csv", "A05929.csv", "A05930.csv", "A05932.csv", "A05933.csv", "A05934.csv", "A05936.csv", "A05937.csv", "A05938.csv", "A05939.csv", "A05940.csv", "A05941.csv", "A05944.csv", "A05945.csv", "A05947.csv", "A05948.csv", "A05949.csv", "A05951.csv", "A05952.csv", "A05957.csv", "A05958.csv", "A05959.csv", "A05963.csv", "A05964.csv", "A05968.csv", "A05975.csv", "A05976.csv", "A05977.csv", "A05979.csv", "A05982.csv", "A05985.csv", "A05988.csv", "A05990.csv", "A05991.csv", "A05993.csv", "A05995.csv", "A05998.csv", "A05999.csv", "A06001.csv", "A06006.csv", "A06007.csv", "A06009.csv", "A06011.csv", "A06014.csv", "A06016.csv", "A06017.csv", "A06018.csv", "A06019.csv", "A06022.csv", "A06024.csv", "A06025.csv", "A06026.csv", "A06027.csv", "A06028.csv", "A06031.csv", "A06032.csv", "A06034.csv", "A06035.csv", "A06036.csv", "A06037.csv", "A06038.csv", "A06039.csv", "A06041.csv", "A06044.csv", "A06045.csv", "A06046.csv", "A06047.csv", "A06049.csv", "A06051.csv", "A06052.csv", "A06053.csv", "A06056.csv", "A06058.csv", "A06059.csv", "A06061.csv", "A06062.csv", "A06063.csv", "A06065.csv", "A06066.csv", "A06068.csv", "A06070.csv", "A06074.csv", "A06075.csv", "A06076.csv", "A06077.csv", "A06079.csv", "A06080.csv", "A06081.csv", "A06082.csv", "A06083.csv", "A06085.csv", "A06087.csv", "A06088.csv", "A06091.csv", "A06093.csv", "A06094.csv", "A06096.csv", "A06097.csv", "A06098.csv", "A06099.csv", "A06102.csv", "A06104.csv", "A06106.csv", "A06107.csv", "A06109.csv", "A06111.csv", "A06113.csv", "A06114.csv", "A06115.csv", "A06117.csv", "A06118.csv", "A06120.csv", "A06122.csv", "A06124.csv", "A06125.csv", "A06127.csv", "A06128.csv", "A06129.csv", "A06130.csv", "A06131.csv", "A06133.csv", "A06136.csv", "A06137.csv", "A06138.csv", "A06139.csv", "A06142.csv", "A06143.csv", "A06144.csv", "A06145.csv", "A06147.csv", "A06148.csv", "A06149.csv", "A06150.csv", "A06151.csv", "A06152.csv", "A06153.csv", "A06157.csv", "A06159.csv", "A06161.csv", "A06162.csv", "A06163.csv", "A06164.csv", "A06165.csv", "A06166.csv", "A06167.csv", "A06168.csv", "A06171.csv", "A06172.csv", "A06173.csv", "A06174.csv", "A06175.csv", "A06177.csv", "A06178.csv", "A06179.csv", "A06181.csv", "A06183.csv", "A06184.csv", "A06185.csv", "A06187.csv", "A06189.csv", "A06191.csv", "A06192.csv", "A06196.csv", "A06197.csv", "A06198.csv", "A06199.csv", "A06200.csv", "A06204.csv", "A06205.csv", "A06206.csv", "A06207.csv", "A06209.csv", "A06211.csv", "A06215.csv", "A06216.csv", "A06220.csv", "A06221.csv", "A06225.csv", "A06227.csv", "A06228.csv", "A06229.csv", "A06232.csv", "A06233.csv", "A06234.csv", "A06235.csv", "A06243.csv", "A06244.csv", "A06249.csv", "A06252.csv", "A06254.csv", "A06255.csv", "A06256.csv", "A06257.csv", "A06258.csv", "A06259.csv", "A06263.csv", "A06264.csv", "A06265.csv", "A06267.csv", "A06270.csv", "A06275.csv", "A06276.csv", "A06277.csv", "A06279.csv", "A06283.csv", "A06284.csv", "A06291.csv", "A06293.csv", "A06294.csv", "A06295.csv", "A06296.csv", "A06302.csv", "A06305.csv", "A06308.csv", "A06309.csv", "A06310.csv", "A06311.csv", "A06313.csv", "A06314.csv", "A06315.csv", "A06316.csv", "A06319.csv", "A06320.csv", "A06324.csv", "A06326.csv", "A06327.csv", "A06328.csv", "A06330.csv", "A06333.csv", "A06334.csv", "A06336.csv", "A06337.csv", "A06341.csv", "A06342.csv", "A06345.csv", "A06348.csv", "A06349.csv", "A06350.csv", "A06351.csv", "A06352.csv", "A06354.csv", "A06355.csv", "A06359.csv", "A06360.csv", "A06361.csv", "A06362.csv", "A06363.csv", "A06364.csv", "A06365.csv", "A06366.csv", "A06370.csv", "A06371.csv", "A06372.csv", "A06375.csv", "A06376.csv", "A06378.csv", "A06379.csv", "A06380.csv", "A06381.csv", "A06382.csv", "A06383.csv", "A06384.csv", "A06385.csv", "A06389.csv", "A06390.csv", "A06392.csv", "A06393.csv", "A06394.csv", "A06395.csv", "A06397.csv", "A06398.csv", "A06399.csv", "A06400.csv", "A06402.csv", "A06404.csv", "A06405.csv", "A06406.csv", "A06407.csv", "A06408.csv", "A06409.csv", "A06410.csv", "A06411.csv", "A06412.csv", "A06414.csv", "A06418.csv", "A06419.csv", "A06420.csv", "A06423.csv", "A06424.csv", "A06425.csv", "A06426.csv", "A06427.csv", "A06429.csv", "A06431.csv", "A06433.csv", "A06437.csv", "A06438.csv", "A06439.csv", "A06441.csv", "A06442.csv", "A06443.csv", "A06445.csv", "A06446.csv", "A06447.csv", "A06448.csv", "A06449.csv", "A06450.csv", "A06453.csv", "A06457.csv", "A06458.csv", "A06459.csv", "A06461.csv", "A06462.csv", "A06463.csv", "A06464.csv", "A06465.csv", "A06466.csv", "A06467.csv", "A06468.csv", "A06469.csv", "A06470.csv", "A06471.csv", "A06473.csv", "A06474.csv", "A06475.csv", "A06476.csv", "A06478.csv", "A06480.csv", "A06481.csv", "A06482.csv", "A06484.csv", "A06486.csv", "A06487.csv", "A06488.csv", "A06489.csv", "A06490.csv", "A06491.csv", "A06492.csv", "A06493.csv", "A06494.csv", "A06495.csv", "A06497.csv", "A06498.csv", "A06499.csv", "A06500.csv", "A06503.csv", "A06505.csv", "A06506.csv", "A06507.csv", "A06508.csv", "A06509.csv", "A06518.csv", "A06519.csv", "A06521.csv", "A06522.csv", "A06523.csv", "A06526.csv", "A06528.csv", "A06529.csv", "A06530.csv", "A06531.csv", "A06535.csv", "A06536.csv", "A06538.csv", "A06539.csv", "A06540.csv", "A06542.csv", "A06543.csv", "A06544.csv", "A06545.csv", "A06547.csv", "A06550.csv", "A06551.csv", "A06552.csv", "A06553.csv", "A06555.csv", "A06557.csv", "A06560.csv", "A06561.csv", "A06563.csv", "A06564.csv", "A06565.csv", "A06566.csv", "A06567.csv", "A06568.csv", "A06569.csv", "A06570.csv", "A06572.csv", "A06573.csv", "A06574.csv", "A06575.csv", "A06576.csv", "A06577.csv", "A06579.csv", "A06580.csv", "A06581.csv", "A06582.csv", "A06583.csv", "A06585.csv", "A06586.csv", "A06588.csv", "A06589.csv", "A06590.csv", "A06591.csv", "A06592.csv", "A06593.csv", "A06594.csv", "A06595.csv", "A06597.csv", "A06598.csv", "A06599.csv", "A06600.csv", "A06601.csv", "A06602.csv", "A06603.csv", "A06604.csv", "A06605.csv", "A06606.csv", "A06607.csv", "A06610.csv", "A06612.csv", "A06615.csv", "A06616.csv", "A06617.csv", "A06618.csv", "A06619.csv", "A06621.csv", "A06622.csv", "A06623.csv", "A06624.csv", "A06627.csv", "A06628.csv", "A06631.csv", "A06634.csv", "A06635.csv", "A06636.csv", "A06637.csv", "A06640.csv", "A06641.csv", "A06643.csv", "A06644.csv", "A06645.csv", "A06646.csv", "A06649.csv", "A06650.csv", "A06651.csv", "A06652.csv", "A06653.csv", "A06654.csv", "A06656.csv", "A06657.csv", "A06659.csv", "A06662.csv", "A06663.csv", "A06665.csv", "A06666.csv", "A06667.csv", "A06668.csv", "A06669.csv", "A06670.csv", "A06671.csv", "A06672.csv", "A06673.csv", "A06674.csv", "A06675.csv", "A06676.csv", "A06677.csv", "A06678.csv", "A06679.csv", "A06681.csv", "A06682.csv", "A06684.csv", "A06686.csv", "A06687.csv", "A06689.csv", "A06690.csv", "A06691.csv", "A06695.csv", "A06696.csv", "A06697.csv", "A06698.csv", "A06699.csv", "A06700.csv", "A06701.csv", "A06702.csv", "A06703.csv", "A06706.csv", "A06707.csv", "A06708.csv", "A06709.csv", "A06710.csv", "A06711.csv", "A06712.csv", "A06713.csv", "A06714.csv", "A06716.csv", "A06718.csv", "A06719.csv", "A06720.csv", "A06721.csv", "A06722.csv", "A06723.csv", "A06725.csv", "A06726.csv", "A06729.csv", "A06730.csv", "A06731.csv", "A06732.csv", "A06733.csv", "A06734.csv", "A06736.csv", "A06738.csv", "A06739.csv", "A06740.csv", "A06743.csv", "A06744.csv", "A06745.csv", "A06746.csv", "A06749.csv", "A06750.csv", "A06751.csv", "A06752.csv", "A06753.csv", "A06755.csv", "A06758.csv", "A06761.csv", "A06763.csv", "A06765.csv", "A06766.csv", "A06768.csv", "A06770.csv", "A06771.csv", "A06774.csv", "A06775.csv", "A06777.csv", "A06778.csv", "A06779.csv", "A06780.csv", "A06781.csv", "A06782.csv", "A06783.csv", "A06784.csv", "A06785.csv", "A06786.csv", "A06787.csv", "A06788.csv", "A06790.csv", "A06791.csv", "A06792.csv", "A06796.csv", "A06797.csv", "A06798.csv", "A06800.csv", "A06802.csv", "A06803.csv", "A06804.csv", "A06805.csv", "A06806.csv", "A06809.csv", "A06810.csv", "A06812.csv", "A06813.csv", "A06814.csv", "A06815.csv", "A06817.csv", "A06818.csv", "A06820.csv", "A06821.csv", "A06822.csv", "A06825.csv", "A06827.csv", "A06828.csv", "A06829.csv", "A06830.csv", "A06832.csv", "A06833.csv", "A06835.csv", "A06836.csv", "A06838.csv", "A06839.csv", "A06840.csv", "A06842.csv", "A06843.csv", "A06844.csv", "A06846.csv", "A06848.csv", "A06849.csv", "A06852.csv", "A06853.csv", "A06854.csv", "A06856.csv", "A06857.csv", "A06858.csv", "A06859.csv", "A06860.csv", "A06861.csv", "A06863.csv", "A06864.csv", "A06865.csv", "A06867.csv", "A06868.csv", "A06869.csv", "A06870.csv", "A06871.csv", "A06872.csv", "A06873.csv", "A06874.csv", "A06875.csv", "A06876.csv", "A06878.csv", "A06879.csv", "A06880.csv", "A06883.csv", "A06884.csv", "A06885.csv", "A06886.csv", "A06889.csv", "A06891.csv", "A06893.csv", "A06894.csv", "A06895.csv", "A06896.csv", "A06898.csv", "A06900.csv", "A06902.csv", "A06903.csv", "A06905.csv", "A06906.csv", "A06908.csv", "A06909.csv", "A06910.csv", "A06911.csv", "A06912.csv", "A06913.csv", "A06915.csv", "A06917.csv", "A06918.csv", "A06922.csv", "A06923.csv", "A06924.csv", "A06925.csv", "A06926.csv", "A06927.csv", "A06928.csv", "A06929.csv", "A06930.csv", "A06931.csv", "A06932.csv", "A06933.csv", "A06934.csv", "A06935.csv", "A06936.csv", "A06937.csv", "A06938.csv", "A06939.csv", "A06940.csv", "A06941.csv", "A06942.csv", "A06943.csv", "A06944.csv", "A06945.csv", "A06946.csv", "A06947.csv", "A06949.csv", "A06950.csv", "A06951.csv", "A06952.csv", "A06954.csv", "A06955.csv", "A06956.csv", "A06957.csv", "A06958.csv", "A06959.csv", "A06960.csv", "A06961.csv", "A06962.csv", "A06965.csv", "A06970.csv", "A06972.csv", "A06973.csv", "A06974.csv", "A06975.csv", "A06976.csv", "A06978.csv", "A06979.csv", "A06980.csv", "A06981.csv", "A06982.csv", "A06983.csv", "A06984.csv", "A06985.csv", "A06988.csv", "A06990.csv", "A06991.csv", "A06993.csv", "A06994.csv", "A06998.csv", "A06999.csv", "A07000.csv"])
#10000 O 15001
with tf.Session() as sess:
	sess.run(init)
	coord=tf.train.Coordinator()
	threads=tf.train.start_queue_runners(coord=coord)
	for i in range(15001):
    		features, labels = sess.run([data_batch, label_batch])
    		b=np.zeros((BATCH_SIZE,2))
    		b[np.arange(BATCH_SIZE), labels]=1
    		# learning rate decay 
    		max_learning_rate = 0.02 
    		min_learning_rate = 0.0001 
    		decay_speed = 1600 
    		learning_rate = min_learning_rate + (max_learning_rate - min_learning_rate) * math.exp(-i/decay_speed)
    		if i%100 == 0:
    			train_accuracy = accuracy.eval(feed_dict= {X: features, Y_: b, tst: False, pkeep: 1.0, pkeep_conv: 1.0})
    			print("step %d, training accuracy %g"%(i, train_accuracy))
    			#tf_confusion_metrics(Y, Y_,session=sess, feed_dict={X: test_set2.data, Y_: c, tst: False, pkeep: 1.0, pkeep_conv: 1.0})
    			#probabilities=Y
    			#print ("probabilities", probabilities.eval(feed_dict={X: test_set.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}))
    		train_step.run(feed_dict={X: features, Y_: b, lr: learning_rate, tst: False, pkeep: 0.75, pkeep_conv: 1.0})
    		update_ema.run(feed_dict={X: features, Y_: b, tst: False, iter: i, pkeep: 1.0, pkeep_conv: 1.0})
	coord.request_stop()
	coord.join(threads)
	#print("test accuracy %g"%accuracy.eval(feed_dict={X: test_set.data, Y_: c, tst: False}))
	probabilities=Y
	#print ("probabilities", probabilities.eval(feed_dict={X: test_set2.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}))
	np.savetxt('result2.txt', probabilities.eval(feed_dict={X: test_set2.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result4.txt', probabilities.eval(feed_dict={X: test_set4.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result7.txt', probabilities.eval(feed_dict={X: test_set7.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result8.txt', probabilities.eval(feed_dict={X: test_set8.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result9.txt', probabilities.eval(feed_dict={X: test_set9.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result10.txt', probabilities.eval(feed_dict={X: test_set10.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result11.txt', probabilities.eval(feed_dict={X: test_set11.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result12.txt', probabilities.eval(feed_dict={X: test_set12.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result15.txt', probabilities.eval(feed_dict={X: test_set15.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result16.txt', probabilities.eval(feed_dict={X: test_set16.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result19.txt', probabilities.eval(feed_dict={X: test_set19.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result20.txt', probabilities.eval(feed_dict={X: test_set20.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result21.txt', probabilities.eval(feed_dict={X: test_set21.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result22.txt', probabilities.eval(feed_dict={X: test_set22.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result23.txt', probabilities.eval(feed_dict={X: test_set23.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result24.txt', probabilities.eval(feed_dict={X: test_set24.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result25.txt', probabilities.eval(feed_dict={X: test_set25.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result26.txt', probabilities.eval(feed_dict={X: test_set26.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result28.txt', probabilities.eval(feed_dict={X: test_set28.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result32.txt', probabilities.eval(feed_dict={X: test_set32.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result33.txt', probabilities.eval(feed_dict={X: test_set33.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result34.txt', probabilities.eval(feed_dict={X: test_set34.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result35.txt', probabilities.eval(feed_dict={X: test_set35.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result36.txt', probabilities.eval(feed_dict={X: test_set36.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result37.txt', probabilities.eval(feed_dict={X: test_set37.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result39.txt', probabilities.eval(feed_dict={X: test_set39.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result40.txt', probabilities.eval(feed_dict={X: test_set40.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result41.txt', probabilities.eval(feed_dict={X: test_set41.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result42.txt', probabilities.eval(feed_dict={X: test_set42.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result43.txt', probabilities.eval(feed_dict={X: test_set43.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result44.txt', probabilities.eval(feed_dict={X: test_set44.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result45.txt', probabilities.eval(feed_dict={X: test_set45.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result47.txt', probabilities.eval(feed_dict={X: test_set47.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result48.txt', probabilities.eval(feed_dict={X: test_set48.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result50.txt', probabilities.eval(feed_dict={X: test_set50.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result51.txt', probabilities.eval(feed_dict={X: test_set51.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result52.txt', probabilities.eval(feed_dict={X: test_set52.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result53.txt', probabilities.eval(feed_dict={X: test_set53.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result54.txt', probabilities.eval(feed_dict={X: test_set54.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result55.txt', probabilities.eval(feed_dict={X: test_set55.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result56.txt', probabilities.eval(feed_dict={X: test_set56.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result57.txt', probabilities.eval(feed_dict={X: test_set57.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result58.txt', probabilities.eval(feed_dict={X: test_set58.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result59.txt', probabilities.eval(feed_dict={X: test_set59.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result60.txt', probabilities.eval(feed_dict={X: test_set60.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result63.txt', probabilities.eval(feed_dict={X: test_set63.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result65.txt', probabilities.eval(feed_dict={X: test_set65.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result70.txt', probabilities.eval(feed_dict={X: test_set70.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result73.txt', probabilities.eval(feed_dict={X: test_set73.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result74.txt', probabilities.eval(feed_dict={X: test_set74.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result75.txt', probabilities.eval(feed_dict={X: test_set75.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result77.txt', probabilities.eval(feed_dict={X: test_set77.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result78.txt', probabilities.eval(feed_dict={X: test_set78.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result79.txt', probabilities.eval(feed_dict={X: test_set79.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result80.txt', probabilities.eval(feed_dict={X: test_set80.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result81.txt', probabilities.eval(feed_dict={X: test_set81.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result82.txt', probabilities.eval(feed_dict={X: test_set82.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result85.txt', probabilities.eval(feed_dict={X: test_set85.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result86.txt', probabilities.eval(feed_dict={X: test_set86.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result88.txt', probabilities.eval(feed_dict={X: test_set88.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result89.txt', probabilities.eval(feed_dict={X: test_set89.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result90.txt', probabilities.eval(feed_dict={X: test_set90.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result92.txt', probabilities.eval(feed_dict={X: test_set92.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result94.txt', probabilities.eval(feed_dict={X: test_set94.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result95.txt', probabilities.eval(feed_dict={X: test_set95.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result96.txt', probabilities.eval(feed_dict={X: test_set96.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result97.txt', probabilities.eval(feed_dict={X: test_set97.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result98.txt', probabilities.eval(feed_dict={X: test_set98.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result100.txt', probabilities.eval(feed_dict={X: test_set100.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result101.txt', probabilities.eval(feed_dict={X: test_set101.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result102.txt', probabilities.eval(feed_dict={X: test_set102.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result103.txt', probabilities.eval(feed_dict={X: test_set103.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result104.txt', probabilities.eval(feed_dict={X: test_set104.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result105.txt', probabilities.eval(feed_dict={X: test_set105.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result106.txt', probabilities.eval(feed_dict={X: test_set106.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result107.txt', probabilities.eval(feed_dict={X: test_set107.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result108.txt', probabilities.eval(feed_dict={X: test_set108.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result109.txt', probabilities.eval(feed_dict={X: test_set109.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result110.txt', probabilities.eval(feed_dict={X: test_set110.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result111.txt', probabilities.eval(feed_dict={X: test_set111.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result112.txt', probabilities.eval(feed_dict={X: test_set112.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result113.txt', probabilities.eval(feed_dict={X: test_set113.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result114.txt', probabilities.eval(feed_dict={X: test_set114.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result115.txt', probabilities.eval(feed_dict={X: test_set115.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result116.txt', probabilities.eval(feed_dict={X: test_set116.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result117.txt', probabilities.eval(feed_dict={X: test_set117.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result118.txt', probabilities.eval(feed_dict={X: test_set118.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result120.txt', probabilities.eval(feed_dict={X: test_set120.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result121.txt', probabilities.eval(feed_dict={X: test_set121.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result122.txt', probabilities.eval(feed_dict={X: test_set122.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result123.txt', probabilities.eval(feed_dict={X: test_set123.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result124.txt', probabilities.eval(feed_dict={X: test_set124.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result125.txt', probabilities.eval(feed_dict={X: test_set125.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result126.txt', probabilities.eval(feed_dict={X: test_set126.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result127.txt', probabilities.eval(feed_dict={X: test_set127.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result128.txt', probabilities.eval(feed_dict={X: test_set128.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result129.txt', probabilities.eval(feed_dict={X: test_set129.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result130.txt', probabilities.eval(feed_dict={X: test_set130.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result131.txt', probabilities.eval(feed_dict={X: test_set131.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result134.txt', probabilities.eval(feed_dict={X: test_set134.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result140.txt', probabilities.eval(feed_dict={X: test_set140.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result141.txt', probabilities.eval(feed_dict={X: test_set141.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result142.txt', probabilities.eval(feed_dict={X: test_set142.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result143.txt', probabilities.eval(feed_dict={X: test_set143.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result146.txt', probabilities.eval(feed_dict={X: test_set146.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result147.txt', probabilities.eval(feed_dict={X: test_set147.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result149.txt', probabilities.eval(feed_dict={X: test_set149.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result151.txt', probabilities.eval(feed_dict={X: test_set151.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result152.txt', probabilities.eval(feed_dict={X: test_set152.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result153.txt', probabilities.eval(feed_dict={X: test_set153.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result158.txt', probabilities.eval(feed_dict={X: test_set158.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result160.txt', probabilities.eval(feed_dict={X: test_set160.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result161.txt', probabilities.eval(feed_dict={X: test_set161.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result163.txt', probabilities.eval(feed_dict={X: test_set163.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result164.txt', probabilities.eval(feed_dict={X: test_set164.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result165.txt', probabilities.eval(feed_dict={X: test_set165.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result167.txt', probabilities.eval(feed_dict={X: test_set167.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result168.txt', probabilities.eval(feed_dict={X: test_set168.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result169.txt', probabilities.eval(feed_dict={X: test_set169.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result170.txt', probabilities.eval(feed_dict={X: test_set170.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result173.txt', probabilities.eval(feed_dict={X: test_set173.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result174.txt', probabilities.eval(feed_dict={X: test_set174.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result175.txt', probabilities.eval(feed_dict={X: test_set175.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result176.txt', probabilities.eval(feed_dict={X: test_set176.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result178.txt', probabilities.eval(feed_dict={X: test_set178.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result180.txt', probabilities.eval(feed_dict={X: test_set180.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result181.txt', probabilities.eval(feed_dict={X: test_set181.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result182.txt', probabilities.eval(feed_dict={X: test_set182.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result183.txt', probabilities.eval(feed_dict={X: test_set183.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result184.txt', probabilities.eval(feed_dict={X: test_set184.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result186.txt', probabilities.eval(feed_dict={X: test_set186.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result188.txt', probabilities.eval(feed_dict={X: test_set188.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result189.txt', probabilities.eval(feed_dict={X: test_set189.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result190.txt', probabilities.eval(feed_dict={X: test_set190.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result191.txt', probabilities.eval(feed_dict={X: test_set191.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result192.txt', probabilities.eval(feed_dict={X: test_set192.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result193.txt', probabilities.eval(feed_dict={X: test_set193.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result196.txt', probabilities.eval(feed_dict={X: test_set196.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result197.txt', probabilities.eval(feed_dict={X: test_set197.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result198.txt', probabilities.eval(feed_dict={X: test_set198.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result199.txt', probabilities.eval(feed_dict={X: test_set199.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result200.txt', probabilities.eval(feed_dict={X: test_set200.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result201.txt', probabilities.eval(feed_dict={X: test_set201.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result204.txt', probabilities.eval(feed_dict={X: test_set204.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result205.txt', probabilities.eval(feed_dict={X: test_set205.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result206.txt', probabilities.eval(feed_dict={X: test_set206.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result207.txt', probabilities.eval(feed_dict={X: test_set207.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result209.txt', probabilities.eval(feed_dict={X: test_set209.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result210.txt', probabilities.eval(feed_dict={X: test_set210.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result211.txt', probabilities.eval(feed_dict={X: test_set211.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result212.txt', probabilities.eval(feed_dict={X: test_set212.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result216.txt', probabilities.eval(feed_dict={X: test_set216.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result218.txt', probabilities.eval(feed_dict={X: test_set218.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result220.txt', probabilities.eval(feed_dict={X: test_set220.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result221.txt', probabilities.eval(feed_dict={X: test_set221.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result222.txt', probabilities.eval(feed_dict={X: test_set222.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result223.txt', probabilities.eval(feed_dict={X: test_set223.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result224.txt', probabilities.eval(feed_dict={X: test_set224.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result225.txt', probabilities.eval(feed_dict={X: test_set225.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result227.txt', probabilities.eval(feed_dict={X: test_set227.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result228.txt', probabilities.eval(feed_dict={X: test_set228.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result230.txt', probabilities.eval(feed_dict={X: test_set230.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result231.txt', probabilities.eval(feed_dict={X: test_set231.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result232.txt', probabilities.eval(feed_dict={X: test_set232.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result234.txt', probabilities.eval(feed_dict={X: test_set234.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result235.txt', probabilities.eval(feed_dict={X: test_set235.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result236.txt', probabilities.eval(feed_dict={X: test_set236.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result238.txt', probabilities.eval(feed_dict={X: test_set238.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result239.txt', probabilities.eval(feed_dict={X: test_set239.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result241.txt', probabilities.eval(feed_dict={X: test_set241.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result242.txt', probabilities.eval(feed_dict={X: test_set242.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result243.txt', probabilities.eval(feed_dict={X: test_set243.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result244.txt', probabilities.eval(feed_dict={X: test_set244.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result246.txt', probabilities.eval(feed_dict={X: test_set246.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result248.txt', probabilities.eval(feed_dict={X: test_set248.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result250.txt', probabilities.eval(feed_dict={X: test_set250.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result253.txt', probabilities.eval(feed_dict={X: test_set253.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result255.txt', probabilities.eval(feed_dict={X: test_set255.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result256.txt', probabilities.eval(feed_dict={X: test_set256.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result257.txt', probabilities.eval(feed_dict={X: test_set257.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result258.txt', probabilities.eval(feed_dict={X: test_set258.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result259.txt', probabilities.eval(feed_dict={X: test_set259.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result260.txt', probabilities.eval(feed_dict={X: test_set260.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result262.txt', probabilities.eval(feed_dict={X: test_set262.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result264.txt', probabilities.eval(feed_dict={X: test_set264.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result266.txt', probabilities.eval(feed_dict={X: test_set266.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result267.txt', probabilities.eval(feed_dict={X: test_set267.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result268.txt', probabilities.eval(feed_dict={X: test_set268.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result269.txt', probabilities.eval(feed_dict={X: test_set269.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result270.txt', probabilities.eval(feed_dict={X: test_set270.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result272.txt', probabilities.eval(feed_dict={X: test_set272.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result273.txt', probabilities.eval(feed_dict={X: test_set273.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result275.txt', probabilities.eval(feed_dict={X: test_set275.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result276.txt', probabilities.eval(feed_dict={X: test_set276.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result278.txt', probabilities.eval(feed_dict={X: test_set278.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result279.txt', probabilities.eval(feed_dict={X: test_set279.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result281.txt', probabilities.eval(feed_dict={X: test_set281.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result282.txt', probabilities.eval(feed_dict={X: test_set282.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result284.txt', probabilities.eval(feed_dict={X: test_set284.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result285.txt', probabilities.eval(feed_dict={X: test_set285.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result287.txt', probabilities.eval(feed_dict={X: test_set287.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result288.txt', probabilities.eval(feed_dict={X: test_set288.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result291.txt', probabilities.eval(feed_dict={X: test_set291.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result293.txt', probabilities.eval(feed_dict={X: test_set293.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result294.txt', probabilities.eval(feed_dict={X: test_set294.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result295.txt', probabilities.eval(feed_dict={X: test_set295.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result296.txt', probabilities.eval(feed_dict={X: test_set296.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result298.txt', probabilities.eval(feed_dict={X: test_set298.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result299.txt', probabilities.eval(feed_dict={X: test_set299.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result300.txt', probabilities.eval(feed_dict={X: test_set300.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result301.txt', probabilities.eval(feed_dict={X: test_set301.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result303.txt', probabilities.eval(feed_dict={X: test_set303.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result304.txt', probabilities.eval(feed_dict={X: test_set304.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result305.txt', probabilities.eval(feed_dict={X: test_set305.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result307.txt', probabilities.eval(feed_dict={X: test_set307.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result309.txt', probabilities.eval(feed_dict={X: test_set309.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result310.txt', probabilities.eval(feed_dict={X: test_set310.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result311.txt', probabilities.eval(feed_dict={X: test_set311.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result312.txt', probabilities.eval(feed_dict={X: test_set312.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result313.txt', probabilities.eval(feed_dict={X: test_set313.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result315.txt', probabilities.eval(feed_dict={X: test_set315.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result317.txt', probabilities.eval(feed_dict={X: test_set317.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result318.txt', probabilities.eval(feed_dict={X: test_set318.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result319.txt', probabilities.eval(feed_dict={X: test_set319.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result323.txt', probabilities.eval(feed_dict={X: test_set323.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result324.txt', probabilities.eval(feed_dict={X: test_set324.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result325.txt', probabilities.eval(feed_dict={X: test_set325.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result326.txt', probabilities.eval(feed_dict={X: test_set326.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result327.txt', probabilities.eval(feed_dict={X: test_set327.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result330.txt', probabilities.eval(feed_dict={X: test_set330.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result331.txt', probabilities.eval(feed_dict={X: test_set331.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result332.txt', probabilities.eval(feed_dict={X: test_set332.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result333.txt', probabilities.eval(feed_dict={X: test_set333.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result334.txt', probabilities.eval(feed_dict={X: test_set334.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result335.txt', probabilities.eval(feed_dict={X: test_set335.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result336.txt', probabilities.eval(feed_dict={X: test_set336.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result337.txt', probabilities.eval(feed_dict={X: test_set337.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result339.txt', probabilities.eval(feed_dict={X: test_set339.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result340.txt', probabilities.eval(feed_dict={X: test_set340.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result341.txt', probabilities.eval(feed_dict={X: test_set341.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result343.txt', probabilities.eval(feed_dict={X: test_set343.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result344.txt', probabilities.eval(feed_dict={X: test_set344.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result345.txt', probabilities.eval(feed_dict={X: test_set345.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result346.txt', probabilities.eval(feed_dict={X: test_set346.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result347.txt', probabilities.eval(feed_dict={X: test_set347.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result349.txt', probabilities.eval(feed_dict={X: test_set349.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result351.txt', probabilities.eval(feed_dict={X: test_set351.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result352.txt', probabilities.eval(feed_dict={X: test_set352.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result353.txt', probabilities.eval(feed_dict={X: test_set353.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result354.txt', probabilities.eval(feed_dict={X: test_set354.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result356.txt', probabilities.eval(feed_dict={X: test_set356.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result357.txt', probabilities.eval(feed_dict={X: test_set357.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result359.txt', probabilities.eval(feed_dict={X: test_set359.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result360.txt', probabilities.eval(feed_dict={X: test_set360.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result361.txt', probabilities.eval(feed_dict={X: test_set361.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result362.txt', probabilities.eval(feed_dict={X: test_set362.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result364.txt', probabilities.eval(feed_dict={X: test_set364.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result365.txt', probabilities.eval(feed_dict={X: test_set365.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result366.txt', probabilities.eval(feed_dict={X: test_set366.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result368.txt', probabilities.eval(feed_dict={X: test_set368.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result369.txt', probabilities.eval(feed_dict={X: test_set369.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result370.txt', probabilities.eval(feed_dict={X: test_set370.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result371.txt', probabilities.eval(feed_dict={X: test_set371.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result372.txt', probabilities.eval(feed_dict={X: test_set372.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result373.txt', probabilities.eval(feed_dict={X: test_set373.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result374.txt', probabilities.eval(feed_dict={X: test_set374.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result375.txt', probabilities.eval(feed_dict={X: test_set375.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result376.txt', probabilities.eval(feed_dict={X: test_set376.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result377.txt', probabilities.eval(feed_dict={X: test_set377.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result378.txt', probabilities.eval(feed_dict={X: test_set378.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result379.txt', probabilities.eval(feed_dict={X: test_set379.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result380.txt', probabilities.eval(feed_dict={X: test_set380.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result381.txt', probabilities.eval(feed_dict={X: test_set381.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result383.txt', probabilities.eval(feed_dict={X: test_set383.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result384.txt', probabilities.eval(feed_dict={X: test_set384.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result385.txt', probabilities.eval(feed_dict={X: test_set385.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result386.txt', probabilities.eval(feed_dict={X: test_set386.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result389.txt', probabilities.eval(feed_dict={X: test_set389.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result390.txt', probabilities.eval(feed_dict={X: test_set390.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result391.txt', probabilities.eval(feed_dict={X: test_set391.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result392.txt', probabilities.eval(feed_dict={X: test_set392.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result393.txt', probabilities.eval(feed_dict={X: test_set393.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result394.txt', probabilities.eval(feed_dict={X: test_set394.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result396.txt', probabilities.eval(feed_dict={X: test_set396.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result397.txt', probabilities.eval(feed_dict={X: test_set397.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result398.txt', probabilities.eval(feed_dict={X: test_set398.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result399.txt', probabilities.eval(feed_dict={X: test_set399.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result400.txt', probabilities.eval(feed_dict={X: test_set400.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result401.txt', probabilities.eval(feed_dict={X: test_set401.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result402.txt', probabilities.eval(feed_dict={X: test_set402.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result403.txt', probabilities.eval(feed_dict={X: test_set403.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result404.txt', probabilities.eval(feed_dict={X: test_set404.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result406.txt', probabilities.eval(feed_dict={X: test_set406.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result407.txt', probabilities.eval(feed_dict={X: test_set407.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result410.txt', probabilities.eval(feed_dict={X: test_set410.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result411.txt', probabilities.eval(feed_dict={X: test_set411.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result412.txt', probabilities.eval(feed_dict={X: test_set412.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result413.txt', probabilities.eval(feed_dict={X: test_set413.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result414.txt', probabilities.eval(feed_dict={X: test_set414.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result415.txt', probabilities.eval(feed_dict={X: test_set415.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result416.txt', probabilities.eval(feed_dict={X: test_set416.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result418.txt', probabilities.eval(feed_dict={X: test_set418.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result420.txt', probabilities.eval(feed_dict={X: test_set420.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result422.txt', probabilities.eval(feed_dict={X: test_set422.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result423.txt', probabilities.eval(feed_dict={X: test_set423.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result424.txt', probabilities.eval(feed_dict={X: test_set424.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result425.txt', probabilities.eval(feed_dict={X: test_set425.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result426.txt', probabilities.eval(feed_dict={X: test_set426.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result427.txt', probabilities.eval(feed_dict={X: test_set427.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result428.txt', probabilities.eval(feed_dict={X: test_set428.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result429.txt', probabilities.eval(feed_dict={X: test_set429.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result431.txt', probabilities.eval(feed_dict={X: test_set431.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result432.txt', probabilities.eval(feed_dict={X: test_set432.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result433.txt', probabilities.eval(feed_dict={X: test_set433.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result434.txt', probabilities.eval(feed_dict={X: test_set434.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result435.txt', probabilities.eval(feed_dict={X: test_set435.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result436.txt', probabilities.eval(feed_dict={X: test_set436.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result437.txt', probabilities.eval(feed_dict={X: test_set437.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result439.txt', probabilities.eval(feed_dict={X: test_set439.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result442.txt', probabilities.eval(feed_dict={X: test_set442.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result443.txt', probabilities.eval(feed_dict={X: test_set443.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result444.txt', probabilities.eval(feed_dict={X: test_set444.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result447.txt', probabilities.eval(feed_dict={X: test_set447.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result449.txt', probabilities.eval(feed_dict={X: test_set449.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result451.txt', probabilities.eval(feed_dict={X: test_set451.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result452.txt', probabilities.eval(feed_dict={X: test_set452.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result453.txt', probabilities.eval(feed_dict={X: test_set453.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result454.txt', probabilities.eval(feed_dict={X: test_set454.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result455.txt', probabilities.eval(feed_dict={X: test_set455.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result457.txt', probabilities.eval(feed_dict={X: test_set457.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result458.txt', probabilities.eval(feed_dict={X: test_set458.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result459.txt', probabilities.eval(feed_dict={X: test_set459.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result461.txt', probabilities.eval(feed_dict={X: test_set461.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result463.txt', probabilities.eval(feed_dict={X: test_set463.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result466.txt', probabilities.eval(feed_dict={X: test_set466.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result467.txt', probabilities.eval(feed_dict={X: test_set467.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result468.txt', probabilities.eval(feed_dict={X: test_set468.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result469.txt', probabilities.eval(feed_dict={X: test_set469.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result470.txt', probabilities.eval(feed_dict={X: test_set470.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result471.txt', probabilities.eval(feed_dict={X: test_set471.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result472.txt', probabilities.eval(feed_dict={X: test_set472.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result473.txt', probabilities.eval(feed_dict={X: test_set473.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result474.txt', probabilities.eval(feed_dict={X: test_set474.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result475.txt', probabilities.eval(feed_dict={X: test_set475.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result476.txt', probabilities.eval(feed_dict={X: test_set476.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result477.txt', probabilities.eval(feed_dict={X: test_set477.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result478.txt', probabilities.eval(feed_dict={X: test_set478.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result479.txt', probabilities.eval(feed_dict={X: test_set479.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result480.txt', probabilities.eval(feed_dict={X: test_set480.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result482.txt', probabilities.eval(feed_dict={X: test_set482.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result483.txt', probabilities.eval(feed_dict={X: test_set483.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result487.txt', probabilities.eval(feed_dict={X: test_set487.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result488.txt', probabilities.eval(feed_dict={X: test_set488.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result490.txt', probabilities.eval(feed_dict={X: test_set490.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result491.txt', probabilities.eval(feed_dict={X: test_set491.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result494.txt', probabilities.eval(feed_dict={X: test_set494.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result495.txt', probabilities.eval(feed_dict={X: test_set495.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result496.txt', probabilities.eval(feed_dict={X: test_set496.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result498.txt', probabilities.eval(feed_dict={X: test_set498.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result499.txt', probabilities.eval(feed_dict={X: test_set499.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result501.txt', probabilities.eval(feed_dict={X: test_set501.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result502.txt', probabilities.eval(feed_dict={X: test_set502.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result503.txt', probabilities.eval(feed_dict={X: test_set503.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result504.txt', probabilities.eval(feed_dict={X: test_set504.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result505.txt', probabilities.eval(feed_dict={X: test_set505.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result507.txt', probabilities.eval(feed_dict={X: test_set507.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result508.txt', probabilities.eval(feed_dict={X: test_set508.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result509.txt', probabilities.eval(feed_dict={X: test_set509.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result511.txt', probabilities.eval(feed_dict={X: test_set511.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result512.txt', probabilities.eval(feed_dict={X: test_set512.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result513.txt', probabilities.eval(feed_dict={X: test_set513.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result514.txt', probabilities.eval(feed_dict={X: test_set514.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result515.txt', probabilities.eval(feed_dict={X: test_set515.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result516.txt', probabilities.eval(feed_dict={X: test_set516.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result518.txt', probabilities.eval(feed_dict={X: test_set518.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result519.txt', probabilities.eval(feed_dict={X: test_set519.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result520.txt', probabilities.eval(feed_dict={X: test_set520.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result521.txt', probabilities.eval(feed_dict={X: test_set521.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result523.txt', probabilities.eval(feed_dict={X: test_set523.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result525.txt', probabilities.eval(feed_dict={X: test_set525.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result528.txt', probabilities.eval(feed_dict={X: test_set528.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result529.txt', probabilities.eval(feed_dict={X: test_set529.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result530.txt', probabilities.eval(feed_dict={X: test_set530.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result532.txt', probabilities.eval(feed_dict={X: test_set532.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result534.txt', probabilities.eval(feed_dict={X: test_set534.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result535.txt', probabilities.eval(feed_dict={X: test_set535.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result536.txt', probabilities.eval(feed_dict={X: test_set536.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result538.txt', probabilities.eval(feed_dict={X: test_set538.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result543.txt', probabilities.eval(feed_dict={X: test_set543.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result544.txt', probabilities.eval(feed_dict={X: test_set544.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result545.txt', probabilities.eval(feed_dict={X: test_set545.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result546.txt', probabilities.eval(feed_dict={X: test_set546.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result548.txt', probabilities.eval(feed_dict={X: test_set548.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result551.txt', probabilities.eval(feed_dict={X: test_set551.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result552.txt', probabilities.eval(feed_dict={X: test_set552.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result553.txt', probabilities.eval(feed_dict={X: test_set553.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result554.txt', probabilities.eval(feed_dict={X: test_set554.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result555.txt', probabilities.eval(feed_dict={X: test_set555.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result557.txt', probabilities.eval(feed_dict={X: test_set557.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result558.txt', probabilities.eval(feed_dict={X: test_set558.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result559.txt', probabilities.eval(feed_dict={X: test_set559.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result561.txt', probabilities.eval(feed_dict={X: test_set561.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result562.txt', probabilities.eval(feed_dict={X: test_set562.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result563.txt', probabilities.eval(feed_dict={X: test_set563.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result566.txt', probabilities.eval(feed_dict={X: test_set566.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result568.txt', probabilities.eval(feed_dict={X: test_set568.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result569.txt', probabilities.eval(feed_dict={X: test_set569.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result571.txt', probabilities.eval(feed_dict={X: test_set571.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result573.txt', probabilities.eval(feed_dict={X: test_set573.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result575.txt', probabilities.eval(feed_dict={X: test_set575.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result576.txt', probabilities.eval(feed_dict={X: test_set576.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result578.txt', probabilities.eval(feed_dict={X: test_set578.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result579.txt', probabilities.eval(feed_dict={X: test_set579.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result582.txt', probabilities.eval(feed_dict={X: test_set582.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result584.txt', probabilities.eval(feed_dict={X: test_set584.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result585.txt', probabilities.eval(feed_dict={X: test_set585.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result586.txt', probabilities.eval(feed_dict={X: test_set586.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result588.txt', probabilities.eval(feed_dict={X: test_set588.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result589.txt', probabilities.eval(feed_dict={X: test_set589.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result590.txt', probabilities.eval(feed_dict={X: test_set590.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result591.txt', probabilities.eval(feed_dict={X: test_set591.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result592.txt', probabilities.eval(feed_dict={X: test_set592.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result593.txt', probabilities.eval(feed_dict={X: test_set593.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result594.txt', probabilities.eval(feed_dict={X: test_set594.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result595.txt', probabilities.eval(feed_dict={X: test_set595.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result596.txt', probabilities.eval(feed_dict={X: test_set596.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result598.txt', probabilities.eval(feed_dict={X: test_set598.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result599.txt', probabilities.eval(feed_dict={X: test_set599.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result600.txt', probabilities.eval(feed_dict={X: test_set600.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result601.txt', probabilities.eval(feed_dict={X: test_set601.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result604.txt', probabilities.eval(feed_dict={X: test_set604.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result607.txt', probabilities.eval(feed_dict={X: test_set607.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result608.txt', probabilities.eval(feed_dict={X: test_set608.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result609.txt', probabilities.eval(feed_dict={X: test_set609.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result611.txt', probabilities.eval(feed_dict={X: test_set611.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result612.txt', probabilities.eval(feed_dict={X: test_set612.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result613.txt', probabilities.eval(feed_dict={X: test_set613.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result614.txt', probabilities.eval(feed_dict={X: test_set614.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result615.txt', probabilities.eval(feed_dict={X: test_set615.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result616.txt', probabilities.eval(feed_dict={X: test_set616.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result619.txt', probabilities.eval(feed_dict={X: test_set619.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result621.txt', probabilities.eval(feed_dict={X: test_set621.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result622.txt', probabilities.eval(feed_dict={X: test_set622.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result623.txt', probabilities.eval(feed_dict={X: test_set623.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result624.txt', probabilities.eval(feed_dict={X: test_set624.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result625.txt', probabilities.eval(feed_dict={X: test_set625.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result626.txt', probabilities.eval(feed_dict={X: test_set626.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result629.txt', probabilities.eval(feed_dict={X: test_set629.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result630.txt', probabilities.eval(feed_dict={X: test_set630.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result631.txt', probabilities.eval(feed_dict={X: test_set631.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result634.txt', probabilities.eval(feed_dict={X: test_set634.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result635.txt', probabilities.eval(feed_dict={X: test_set635.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result639.txt', probabilities.eval(feed_dict={X: test_set639.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result640.txt', probabilities.eval(feed_dict={X: test_set640.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result642.txt', probabilities.eval(feed_dict={X: test_set642.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result644.txt', probabilities.eval(feed_dict={X: test_set644.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result645.txt', probabilities.eval(feed_dict={X: test_set645.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result646.txt', probabilities.eval(feed_dict={X: test_set646.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result647.txt', probabilities.eval(feed_dict={X: test_set647.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result650.txt', probabilities.eval(feed_dict={X: test_set650.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result651.txt', probabilities.eval(feed_dict={X: test_set651.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result652.txt', probabilities.eval(feed_dict={X: test_set652.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result653.txt', probabilities.eval(feed_dict={X: test_set653.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result654.txt', probabilities.eval(feed_dict={X: test_set654.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result655.txt', probabilities.eval(feed_dict={X: test_set655.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result656.txt', probabilities.eval(feed_dict={X: test_set656.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result657.txt', probabilities.eval(feed_dict={X: test_set657.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result660.txt', probabilities.eval(feed_dict={X: test_set660.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result661.txt', probabilities.eval(feed_dict={X: test_set661.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result662.txt', probabilities.eval(feed_dict={X: test_set662.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result663.txt', probabilities.eval(feed_dict={X: test_set663.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result664.txt', probabilities.eval(feed_dict={X: test_set664.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result665.txt', probabilities.eval(feed_dict={X: test_set665.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result666.txt', probabilities.eval(feed_dict={X: test_set666.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result667.txt', probabilities.eval(feed_dict={X: test_set667.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result668.txt', probabilities.eval(feed_dict={X: test_set668.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result669.txt', probabilities.eval(feed_dict={X: test_set669.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result671.txt', probabilities.eval(feed_dict={X: test_set671.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result673.txt', probabilities.eval(feed_dict={X: test_set673.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result675.txt', probabilities.eval(feed_dict={X: test_set675.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result676.txt', probabilities.eval(feed_dict={X: test_set676.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result677.txt', probabilities.eval(feed_dict={X: test_set677.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result680.txt', probabilities.eval(feed_dict={X: test_set680.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result681.txt', probabilities.eval(feed_dict={X: test_set681.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result682.txt', probabilities.eval(feed_dict={X: test_set682.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result683.txt', probabilities.eval(feed_dict={X: test_set683.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result684.txt', probabilities.eval(feed_dict={X: test_set684.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result685.txt', probabilities.eval(feed_dict={X: test_set685.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result687.txt', probabilities.eval(feed_dict={X: test_set687.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result688.txt', probabilities.eval(feed_dict={X: test_set688.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result690.txt', probabilities.eval(feed_dict={X: test_set690.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result692.txt', probabilities.eval(feed_dict={X: test_set692.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result693.txt', probabilities.eval(feed_dict={X: test_set693.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result694.txt', probabilities.eval(feed_dict={X: test_set694.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result695.txt', probabilities.eval(feed_dict={X: test_set695.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result697.txt', probabilities.eval(feed_dict={X: test_set697.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result698.txt', probabilities.eval(feed_dict={X: test_set698.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result699.txt', probabilities.eval(feed_dict={X: test_set699.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result700.txt', probabilities.eval(feed_dict={X: test_set700.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result704.txt', probabilities.eval(feed_dict={X: test_set704.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result705.txt', probabilities.eval(feed_dict={X: test_set705.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result706.txt', probabilities.eval(feed_dict={X: test_set706.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result707.txt', probabilities.eval(feed_dict={X: test_set707.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result709.txt', probabilities.eval(feed_dict={X: test_set709.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result710.txt', probabilities.eval(feed_dict={X: test_set710.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result712.txt', probabilities.eval(feed_dict={X: test_set712.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result714.txt', probabilities.eval(feed_dict={X: test_set714.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result715.txt', probabilities.eval(feed_dict={X: test_set715.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result716.txt', probabilities.eval(feed_dict={X: test_set716.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result717.txt', probabilities.eval(feed_dict={X: test_set717.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result718.txt', probabilities.eval(feed_dict={X: test_set718.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result719.txt', probabilities.eval(feed_dict={X: test_set719.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result721.txt', probabilities.eval(feed_dict={X: test_set721.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result722.txt', probabilities.eval(feed_dict={X: test_set722.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result725.txt', probabilities.eval(feed_dict={X: test_set725.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result728.txt', probabilities.eval(feed_dict={X: test_set728.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result729.txt', probabilities.eval(feed_dict={X: test_set729.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result730.txt', probabilities.eval(feed_dict={X: test_set730.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result732.txt', probabilities.eval(feed_dict={X: test_set732.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result735.txt', probabilities.eval(feed_dict={X: test_set735.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result736.txt', probabilities.eval(feed_dict={X: test_set736.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result738.txt', probabilities.eval(feed_dict={X: test_set738.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result739.txt', probabilities.eval(feed_dict={X: test_set739.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result743.txt', probabilities.eval(feed_dict={X: test_set743.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result744.txt', probabilities.eval(feed_dict={X: test_set744.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result745.txt', probabilities.eval(feed_dict={X: test_set745.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result746.txt', probabilities.eval(feed_dict={X: test_set746.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result747.txt', probabilities.eval(feed_dict={X: test_set747.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result748.txt', probabilities.eval(feed_dict={X: test_set748.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result749.txt', probabilities.eval(feed_dict={X: test_set749.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result750.txt', probabilities.eval(feed_dict={X: test_set750.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result751.txt', probabilities.eval(feed_dict={X: test_set751.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result753.txt', probabilities.eval(feed_dict={X: test_set753.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result755.txt', probabilities.eval(feed_dict={X: test_set755.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result757.txt', probabilities.eval(feed_dict={X: test_set757.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result758.txt', probabilities.eval(feed_dict={X: test_set758.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result759.txt', probabilities.eval(feed_dict={X: test_set759.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result761.txt', probabilities.eval(feed_dict={X: test_set761.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result762.txt', probabilities.eval(feed_dict={X: test_set762.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result763.txt', probabilities.eval(feed_dict={X: test_set763.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result764.txt', probabilities.eval(feed_dict={X: test_set764.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result765.txt', probabilities.eval(feed_dict={X: test_set765.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result766.txt', probabilities.eval(feed_dict={X: test_set766.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result767.txt', probabilities.eval(feed_dict={X: test_set767.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result769.txt', probabilities.eval(feed_dict={X: test_set769.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result770.txt', probabilities.eval(feed_dict={X: test_set770.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result771.txt', probabilities.eval(feed_dict={X: test_set771.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result774.txt', probabilities.eval(feed_dict={X: test_set774.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result775.txt', probabilities.eval(feed_dict={X: test_set775.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result778.txt', probabilities.eval(feed_dict={X: test_set778.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result780.txt', probabilities.eval(feed_dict={X: test_set780.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result782.txt', probabilities.eval(feed_dict={X: test_set782.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result783.txt', probabilities.eval(feed_dict={X: test_set783.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result784.txt', probabilities.eval(feed_dict={X: test_set784.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result788.txt', probabilities.eval(feed_dict={X: test_set788.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result791.txt', probabilities.eval(feed_dict={X: test_set791.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result792.txt', probabilities.eval(feed_dict={X: test_set792.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result793.txt', probabilities.eval(feed_dict={X: test_set793.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result795.txt', probabilities.eval(feed_dict={X: test_set795.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result798.txt', probabilities.eval(feed_dict={X: test_set798.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result800.txt', probabilities.eval(feed_dict={X: test_set800.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result803.txt', probabilities.eval(feed_dict={X: test_set803.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result804.txt', probabilities.eval(feed_dict={X: test_set804.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result805.txt', probabilities.eval(feed_dict={X: test_set805.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result806.txt', probabilities.eval(feed_dict={X: test_set806.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result807.txt', probabilities.eval(feed_dict={X: test_set807.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result810.txt', probabilities.eval(feed_dict={X: test_set810.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result811.txt', probabilities.eval(feed_dict={X: test_set811.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result812.txt', probabilities.eval(feed_dict={X: test_set812.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result813.txt', probabilities.eval(feed_dict={X: test_set813.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result814.txt', probabilities.eval(feed_dict={X: test_set814.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result817.txt', probabilities.eval(feed_dict={X: test_set817.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result818.txt', probabilities.eval(feed_dict={X: test_set818.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result819.txt', probabilities.eval(feed_dict={X: test_set819.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result820.txt', probabilities.eval(feed_dict={X: test_set820.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result822.txt', probabilities.eval(feed_dict={X: test_set822.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result823.txt', probabilities.eval(feed_dict={X: test_set823.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result824.txt', probabilities.eval(feed_dict={X: test_set824.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result826.txt', probabilities.eval(feed_dict={X: test_set826.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result828.txt', probabilities.eval(feed_dict={X: test_set828.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result829.txt', probabilities.eval(feed_dict={X: test_set829.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result832.txt', probabilities.eval(feed_dict={X: test_set832.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result834.txt', probabilities.eval(feed_dict={X: test_set834.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result835.txt', probabilities.eval(feed_dict={X: test_set835.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result836.txt', probabilities.eval(feed_dict={X: test_set836.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result837.txt', probabilities.eval(feed_dict={X: test_set837.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result838.txt', probabilities.eval(feed_dict={X: test_set838.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result839.txt', probabilities.eval(feed_dict={X: test_set839.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result841.txt', probabilities.eval(feed_dict={X: test_set841.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result842.txt', probabilities.eval(feed_dict={X: test_set842.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result843.txt', probabilities.eval(feed_dict={X: test_set843.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result844.txt', probabilities.eval(feed_dict={X: test_set844.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result846.txt', probabilities.eval(feed_dict={X: test_set846.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result847.txt', probabilities.eval(feed_dict={X: test_set847.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result848.txt', probabilities.eval(feed_dict={X: test_set848.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result849.txt', probabilities.eval(feed_dict={X: test_set849.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result851.txt', probabilities.eval(feed_dict={X: test_set851.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result852.txt', probabilities.eval(feed_dict={X: test_set852.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result854.txt', probabilities.eval(feed_dict={X: test_set854.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result855.txt', probabilities.eval(feed_dict={X: test_set855.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result856.txt', probabilities.eval(feed_dict={X: test_set856.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result858.txt', probabilities.eval(feed_dict={X: test_set858.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result859.txt', probabilities.eval(feed_dict={X: test_set859.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result860.txt', probabilities.eval(feed_dict={X: test_set860.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result861.txt', probabilities.eval(feed_dict={X: test_set861.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result862.txt', probabilities.eval(feed_dict={X: test_set862.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result863.txt', probabilities.eval(feed_dict={X: test_set863.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result864.txt', probabilities.eval(feed_dict={X: test_set864.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result866.txt', probabilities.eval(feed_dict={X: test_set866.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result868.txt', probabilities.eval(feed_dict={X: test_set868.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result870.txt', probabilities.eval(feed_dict={X: test_set870.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result871.txt', probabilities.eval(feed_dict={X: test_set871.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result872.txt', probabilities.eval(feed_dict={X: test_set872.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result873.txt', probabilities.eval(feed_dict={X: test_set873.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result875.txt', probabilities.eval(feed_dict={X: test_set875.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result876.txt', probabilities.eval(feed_dict={X: test_set876.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result877.txt', probabilities.eval(feed_dict={X: test_set877.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result882.txt', probabilities.eval(feed_dict={X: test_set882.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result884.txt', probabilities.eval(feed_dict={X: test_set884.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result885.txt', probabilities.eval(feed_dict={X: test_set885.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result886.txt', probabilities.eval(feed_dict={X: test_set886.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result888.txt', probabilities.eval(feed_dict={X: test_set888.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result889.txt', probabilities.eval(feed_dict={X: test_set889.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result893.txt', probabilities.eval(feed_dict={X: test_set893.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result896.txt', probabilities.eval(feed_dict={X: test_set896.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result897.txt', probabilities.eval(feed_dict={X: test_set897.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result898.txt', probabilities.eval(feed_dict={X: test_set898.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result901.txt', probabilities.eval(feed_dict={X: test_set901.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result903.txt', probabilities.eval(feed_dict={X: test_set903.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result904.txt', probabilities.eval(feed_dict={X: test_set904.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result905.txt', probabilities.eval(feed_dict={X: test_set905.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result906.txt', probabilities.eval(feed_dict={X: test_set906.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result907.txt', probabilities.eval(feed_dict={X: test_set907.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result909.txt', probabilities.eval(feed_dict={X: test_set909.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result910.txt', probabilities.eval(feed_dict={X: test_set910.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result911.txt', probabilities.eval(feed_dict={X: test_set911.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result912.txt', probabilities.eval(feed_dict={X: test_set912.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result916.txt', probabilities.eval(feed_dict={X: test_set916.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result917.txt', probabilities.eval(feed_dict={X: test_set917.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result918.txt', probabilities.eval(feed_dict={X: test_set918.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result919.txt', probabilities.eval(feed_dict={X: test_set919.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result922.txt', probabilities.eval(feed_dict={X: test_set922.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result924.txt', probabilities.eval(feed_dict={X: test_set924.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result925.txt', probabilities.eval(feed_dict={X: test_set925.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result926.txt', probabilities.eval(feed_dict={X: test_set926.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result927.txt', probabilities.eval(feed_dict={X: test_set927.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result929.txt', probabilities.eval(feed_dict={X: test_set929.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result930.txt', probabilities.eval(feed_dict={X: test_set930.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result931.txt', probabilities.eval(feed_dict={X: test_set931.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result932.txt', probabilities.eval(feed_dict={X: test_set932.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result933.txt', probabilities.eval(feed_dict={X: test_set933.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result935.txt', probabilities.eval(feed_dict={X: test_set935.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result937.txt', probabilities.eval(feed_dict={X: test_set937.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result941.txt', probabilities.eval(feed_dict={X: test_set941.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result943.txt', probabilities.eval(feed_dict={X: test_set943.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result944.txt', probabilities.eval(feed_dict={X: test_set944.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result945.txt', probabilities.eval(feed_dict={X: test_set945.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result946.txt', probabilities.eval(feed_dict={X: test_set946.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result947.txt', probabilities.eval(feed_dict={X: test_set947.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result948.txt', probabilities.eval(feed_dict={X: test_set948.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result949.txt', probabilities.eval(feed_dict={X: test_set949.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result950.txt', probabilities.eval(feed_dict={X: test_set950.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result951.txt', probabilities.eval(feed_dict={X: test_set951.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result953.txt', probabilities.eval(feed_dict={X: test_set953.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result955.txt', probabilities.eval(feed_dict={X: test_set955.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result956.txt', probabilities.eval(feed_dict={X: test_set956.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result957.txt', probabilities.eval(feed_dict={X: test_set957.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result958.txt', probabilities.eval(feed_dict={X: test_set958.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result960.txt', probabilities.eval(feed_dict={X: test_set960.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result962.txt', probabilities.eval(feed_dict={X: test_set962.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result964.txt', probabilities.eval(feed_dict={X: test_set964.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result965.txt', probabilities.eval(feed_dict={X: test_set965.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result967.txt', probabilities.eval(feed_dict={X: test_set967.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result969.txt', probabilities.eval(feed_dict={X: test_set969.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result970.txt', probabilities.eval(feed_dict={X: test_set970.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result972.txt', probabilities.eval(feed_dict={X: test_set972.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result974.txt', probabilities.eval(feed_dict={X: test_set974.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result975.txt', probabilities.eval(feed_dict={X: test_set975.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result979.txt', probabilities.eval(feed_dict={X: test_set979.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result981.txt', probabilities.eval(feed_dict={X: test_set981.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result982.txt', probabilities.eval(feed_dict={X: test_set982.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result983.txt', probabilities.eval(feed_dict={X: test_set983.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result984.txt', probabilities.eval(feed_dict={X: test_set984.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result987.txt', probabilities.eval(feed_dict={X: test_set987.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result989.txt', probabilities.eval(feed_dict={X: test_set989.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result991.txt', probabilities.eval(feed_dict={X: test_set991.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result993.txt', probabilities.eval(feed_dict={X: test_set993.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result994.txt', probabilities.eval(feed_dict={X: test_set994.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result995.txt', probabilities.eval(feed_dict={X: test_set995.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result997.txt', probabilities.eval(feed_dict={X: test_set997.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result999.txt', probabilities.eval(feed_dict={X: test_set999.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1000.txt', probabilities.eval(feed_dict={X: test_set1000.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1001.txt', probabilities.eval(feed_dict={X: test_set1001.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1002.txt', probabilities.eval(feed_dict={X: test_set1002.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1003.txt', probabilities.eval(feed_dict={X: test_set1003.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1004.txt', probabilities.eval(feed_dict={X: test_set1004.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1006.txt', probabilities.eval(feed_dict={X: test_set1006.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1009.txt', probabilities.eval(feed_dict={X: test_set1009.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1011.txt', probabilities.eval(feed_dict={X: test_set1011.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1012.txt', probabilities.eval(feed_dict={X: test_set1012.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1013.txt', probabilities.eval(feed_dict={X: test_set1013.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1014.txt', probabilities.eval(feed_dict={X: test_set1014.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1015.txt', probabilities.eval(feed_dict={X: test_set1015.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1016.txt', probabilities.eval(feed_dict={X: test_set1016.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1018.txt', probabilities.eval(feed_dict={X: test_set1018.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1020.txt', probabilities.eval(feed_dict={X: test_set1020.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1022.txt', probabilities.eval(feed_dict={X: test_set1022.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1023.txt', probabilities.eval(feed_dict={X: test_set1023.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1025.txt', probabilities.eval(feed_dict={X: test_set1025.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1026.txt', probabilities.eval(feed_dict={X: test_set1026.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1028.txt', probabilities.eval(feed_dict={X: test_set1028.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1029.txt', probabilities.eval(feed_dict={X: test_set1029.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1031.txt', probabilities.eval(feed_dict={X: test_set1031.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1032.txt', probabilities.eval(feed_dict={X: test_set1032.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1033.txt', probabilities.eval(feed_dict={X: test_set1033.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1038.txt', probabilities.eval(feed_dict={X: test_set1038.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1041.txt', probabilities.eval(feed_dict={X: test_set1041.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1043.txt', probabilities.eval(feed_dict={X: test_set1043.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1044.txt', probabilities.eval(feed_dict={X: test_set1044.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1046.txt', probabilities.eval(feed_dict={X: test_set1046.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1049.txt', probabilities.eval(feed_dict={X: test_set1049.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1051.txt', probabilities.eval(feed_dict={X: test_set1051.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1052.txt', probabilities.eval(feed_dict={X: test_set1052.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1053.txt', probabilities.eval(feed_dict={X: test_set1053.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1055.txt', probabilities.eval(feed_dict={X: test_set1055.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1057.txt', probabilities.eval(feed_dict={X: test_set1057.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1062.txt', probabilities.eval(feed_dict={X: test_set1062.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1063.txt', probabilities.eval(feed_dict={X: test_set1063.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1064.txt', probabilities.eval(feed_dict={X: test_set1064.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1065.txt', probabilities.eval(feed_dict={X: test_set1065.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1066.txt', probabilities.eval(feed_dict={X: test_set1066.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1067.txt', probabilities.eval(feed_dict={X: test_set1067.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1068.txt', probabilities.eval(feed_dict={X: test_set1068.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1069.txt', probabilities.eval(feed_dict={X: test_set1069.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1072.txt', probabilities.eval(feed_dict={X: test_set1072.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1073.txt', probabilities.eval(feed_dict={X: test_set1073.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1074.txt', probabilities.eval(feed_dict={X: test_set1074.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1075.txt', probabilities.eval(feed_dict={X: test_set1075.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1077.txt', probabilities.eval(feed_dict={X: test_set1077.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1078.txt', probabilities.eval(feed_dict={X: test_set1078.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1079.txt', probabilities.eval(feed_dict={X: test_set1079.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1080.txt', probabilities.eval(feed_dict={X: test_set1080.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1082.txt', probabilities.eval(feed_dict={X: test_set1082.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1083.txt', probabilities.eval(feed_dict={X: test_set1083.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1084.txt', probabilities.eval(feed_dict={X: test_set1084.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1085.txt', probabilities.eval(feed_dict={X: test_set1085.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1088.txt', probabilities.eval(feed_dict={X: test_set1088.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1089.txt', probabilities.eval(feed_dict={X: test_set1089.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1091.txt', probabilities.eval(feed_dict={X: test_set1091.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1092.txt', probabilities.eval(feed_dict={X: test_set1092.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1094.txt', probabilities.eval(feed_dict={X: test_set1094.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1095.txt', probabilities.eval(feed_dict={X: test_set1095.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1097.txt', probabilities.eval(feed_dict={X: test_set1097.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1098.txt', probabilities.eval(feed_dict={X: test_set1098.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1099.txt', probabilities.eval(feed_dict={X: test_set1099.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1100.txt', probabilities.eval(feed_dict={X: test_set1100.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1102.txt', probabilities.eval(feed_dict={X: test_set1102.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1103.txt', probabilities.eval(feed_dict={X: test_set1103.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1105.txt', probabilities.eval(feed_dict={X: test_set1105.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1106.txt', probabilities.eval(feed_dict={X: test_set1106.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1107.txt', probabilities.eval(feed_dict={X: test_set1107.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1108.txt', probabilities.eval(feed_dict={X: test_set1108.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1109.txt', probabilities.eval(feed_dict={X: test_set1109.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1110.txt', probabilities.eval(feed_dict={X: test_set1110.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1111.txt', probabilities.eval(feed_dict={X: test_set1111.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1113.txt', probabilities.eval(feed_dict={X: test_set1113.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1115.txt', probabilities.eval(feed_dict={X: test_set1115.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1116.txt', probabilities.eval(feed_dict={X: test_set1116.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1117.txt', probabilities.eval(feed_dict={X: test_set1117.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1119.txt', probabilities.eval(feed_dict={X: test_set1119.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1120.txt', probabilities.eval(feed_dict={X: test_set1120.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1121.txt', probabilities.eval(feed_dict={X: test_set1121.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1122.txt', probabilities.eval(feed_dict={X: test_set1122.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1123.txt', probabilities.eval(feed_dict={X: test_set1123.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1124.txt', probabilities.eval(feed_dict={X: test_set1124.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1125.txt', probabilities.eval(feed_dict={X: test_set1125.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1127.txt', probabilities.eval(feed_dict={X: test_set1127.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1128.txt', probabilities.eval(feed_dict={X: test_set1128.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1129.txt', probabilities.eval(feed_dict={X: test_set1129.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1130.txt', probabilities.eval(feed_dict={X: test_set1130.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1131.txt', probabilities.eval(feed_dict={X: test_set1131.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1132.txt', probabilities.eval(feed_dict={X: test_set1132.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1135.txt', probabilities.eval(feed_dict={X: test_set1135.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1136.txt', probabilities.eval(feed_dict={X: test_set1136.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1137.txt', probabilities.eval(feed_dict={X: test_set1137.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1138.txt', probabilities.eval(feed_dict={X: test_set1138.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1140.txt', probabilities.eval(feed_dict={X: test_set1140.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1141.txt', probabilities.eval(feed_dict={X: test_set1141.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1143.txt', probabilities.eval(feed_dict={X: test_set1143.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1144.txt', probabilities.eval(feed_dict={X: test_set1144.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1145.txt', probabilities.eval(feed_dict={X: test_set1145.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1150.txt', probabilities.eval(feed_dict={X: test_set1150.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1151.txt', probabilities.eval(feed_dict={X: test_set1151.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1152.txt', probabilities.eval(feed_dict={X: test_set1152.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1154.txt', probabilities.eval(feed_dict={X: test_set1154.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1155.txt', probabilities.eval(feed_dict={X: test_set1155.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1156.txt', probabilities.eval(feed_dict={X: test_set1156.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1157.txt', probabilities.eval(feed_dict={X: test_set1157.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1158.txt', probabilities.eval(feed_dict={X: test_set1158.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1161.txt', probabilities.eval(feed_dict={X: test_set1161.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1162.txt', probabilities.eval(feed_dict={X: test_set1162.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1165.txt', probabilities.eval(feed_dict={X: test_set1165.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1168.txt', probabilities.eval(feed_dict={X: test_set1168.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1169.txt', probabilities.eval(feed_dict={X: test_set1169.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1170.txt', probabilities.eval(feed_dict={X: test_set1170.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1171.txt', probabilities.eval(feed_dict={X: test_set1171.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1172.txt', probabilities.eval(feed_dict={X: test_set1172.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1173.txt', probabilities.eval(feed_dict={X: test_set1173.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1174.txt', probabilities.eval(feed_dict={X: test_set1174.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1177.txt', probabilities.eval(feed_dict={X: test_set1177.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1178.txt', probabilities.eval(feed_dict={X: test_set1178.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1180.txt', probabilities.eval(feed_dict={X: test_set1180.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1182.txt', probabilities.eval(feed_dict={X: test_set1182.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1183.txt', probabilities.eval(feed_dict={X: test_set1183.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1184.txt', probabilities.eval(feed_dict={X: test_set1184.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1186.txt', probabilities.eval(feed_dict={X: test_set1186.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1187.txt', probabilities.eval(feed_dict={X: test_set1187.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1188.txt', probabilities.eval(feed_dict={X: test_set1188.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1189.txt', probabilities.eval(feed_dict={X: test_set1189.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1191.txt', probabilities.eval(feed_dict={X: test_set1191.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1192.txt', probabilities.eval(feed_dict={X: test_set1192.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1193.txt', probabilities.eval(feed_dict={X: test_set1193.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1196.txt', probabilities.eval(feed_dict={X: test_set1196.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1197.txt', probabilities.eval(feed_dict={X: test_set1197.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1198.txt', probabilities.eval(feed_dict={X: test_set1198.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1199.txt', probabilities.eval(feed_dict={X: test_set1199.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1201.txt', probabilities.eval(feed_dict={X: test_set1201.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1202.txt', probabilities.eval(feed_dict={X: test_set1202.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1204.txt', probabilities.eval(feed_dict={X: test_set1204.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1205.txt', probabilities.eval(feed_dict={X: test_set1205.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1206.txt', probabilities.eval(feed_dict={X: test_set1206.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1207.txt', probabilities.eval(feed_dict={X: test_set1207.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1212.txt', probabilities.eval(feed_dict={X: test_set1212.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1214.txt', probabilities.eval(feed_dict={X: test_set1214.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1215.txt', probabilities.eval(feed_dict={X: test_set1215.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1218.txt', probabilities.eval(feed_dict={X: test_set1218.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1219.txt', probabilities.eval(feed_dict={X: test_set1219.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1220.txt', probabilities.eval(feed_dict={X: test_set1220.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1222.txt', probabilities.eval(feed_dict={X: test_set1222.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1223.txt', probabilities.eval(feed_dict={X: test_set1223.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1224.txt', probabilities.eval(feed_dict={X: test_set1224.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1225.txt', probabilities.eval(feed_dict={X: test_set1225.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1226.txt', probabilities.eval(feed_dict={X: test_set1226.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1227.txt', probabilities.eval(feed_dict={X: test_set1227.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1228.txt', probabilities.eval(feed_dict={X: test_set1228.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1231.txt', probabilities.eval(feed_dict={X: test_set1231.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1232.txt', probabilities.eval(feed_dict={X: test_set1232.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1233.txt', probabilities.eval(feed_dict={X: test_set1233.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1234.txt', probabilities.eval(feed_dict={X: test_set1234.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1235.txt', probabilities.eval(feed_dict={X: test_set1235.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1236.txt', probabilities.eval(feed_dict={X: test_set1236.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1237.txt', probabilities.eval(feed_dict={X: test_set1237.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1238.txt', probabilities.eval(feed_dict={X: test_set1238.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1239.txt', probabilities.eval(feed_dict={X: test_set1239.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1240.txt', probabilities.eval(feed_dict={X: test_set1240.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1242.txt', probabilities.eval(feed_dict={X: test_set1242.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1243.txt', probabilities.eval(feed_dict={X: test_set1243.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1244.txt', probabilities.eval(feed_dict={X: test_set1244.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1245.txt', probabilities.eval(feed_dict={X: test_set1245.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1248.txt', probabilities.eval(feed_dict={X: test_set1248.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1252.txt', probabilities.eval(feed_dict={X: test_set1252.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1254.txt', probabilities.eval(feed_dict={X: test_set1254.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1255.txt', probabilities.eval(feed_dict={X: test_set1255.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1257.txt', probabilities.eval(feed_dict={X: test_set1257.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1258.txt', probabilities.eval(feed_dict={X: test_set1258.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1259.txt', probabilities.eval(feed_dict={X: test_set1259.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1260.txt', probabilities.eval(feed_dict={X: test_set1260.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1261.txt', probabilities.eval(feed_dict={X: test_set1261.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1263.txt', probabilities.eval(feed_dict={X: test_set1263.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1264.txt', probabilities.eval(feed_dict={X: test_set1264.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1265.txt', probabilities.eval(feed_dict={X: test_set1265.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1270.txt', probabilities.eval(feed_dict={X: test_set1270.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1271.txt', probabilities.eval(feed_dict={X: test_set1271.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1272.txt', probabilities.eval(feed_dict={X: test_set1272.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1274.txt', probabilities.eval(feed_dict={X: test_set1274.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1275.txt', probabilities.eval(feed_dict={X: test_set1275.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1277.txt', probabilities.eval(feed_dict={X: test_set1277.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1279.txt', probabilities.eval(feed_dict={X: test_set1279.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1280.txt', probabilities.eval(feed_dict={X: test_set1280.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1281.txt', probabilities.eval(feed_dict={X: test_set1281.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1282.txt', probabilities.eval(feed_dict={X: test_set1282.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1283.txt', probabilities.eval(feed_dict={X: test_set1283.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1284.txt', probabilities.eval(feed_dict={X: test_set1284.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1286.txt', probabilities.eval(feed_dict={X: test_set1286.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1287.txt', probabilities.eval(feed_dict={X: test_set1287.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1288.txt', probabilities.eval(feed_dict={X: test_set1288.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1289.txt', probabilities.eval(feed_dict={X: test_set1289.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1290.txt', probabilities.eval(feed_dict={X: test_set1290.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1295.txt', probabilities.eval(feed_dict={X: test_set1295.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1296.txt', probabilities.eval(feed_dict={X: test_set1296.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1297.txt', probabilities.eval(feed_dict={X: test_set1297.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1298.txt', probabilities.eval(feed_dict={X: test_set1298.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1300.txt', probabilities.eval(feed_dict={X: test_set1300.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1302.txt', probabilities.eval(feed_dict={X: test_set1302.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1304.txt', probabilities.eval(feed_dict={X: test_set1304.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1305.txt', probabilities.eval(feed_dict={X: test_set1305.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1306.txt', probabilities.eval(feed_dict={X: test_set1306.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1307.txt', probabilities.eval(feed_dict={X: test_set1307.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1308.txt', probabilities.eval(feed_dict={X: test_set1308.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1315.txt', probabilities.eval(feed_dict={X: test_set1315.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1316.txt', probabilities.eval(feed_dict={X: test_set1316.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1318.txt', probabilities.eval(feed_dict={X: test_set1318.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1319.txt', probabilities.eval(feed_dict={X: test_set1319.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1321.txt', probabilities.eval(feed_dict={X: test_set1321.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1322.txt', probabilities.eval(feed_dict={X: test_set1322.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1323.txt', probabilities.eval(feed_dict={X: test_set1323.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1324.txt', probabilities.eval(feed_dict={X: test_set1324.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1325.txt', probabilities.eval(feed_dict={X: test_set1325.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1326.txt', probabilities.eval(feed_dict={X: test_set1326.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1327.txt', probabilities.eval(feed_dict={X: test_set1327.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1328.txt', probabilities.eval(feed_dict={X: test_set1328.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1330.txt', probabilities.eval(feed_dict={X: test_set1330.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1333.txt', probabilities.eval(feed_dict={X: test_set1333.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1334.txt', probabilities.eval(feed_dict={X: test_set1334.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1337.txt', probabilities.eval(feed_dict={X: test_set1337.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1338.txt', probabilities.eval(feed_dict={X: test_set1338.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1340.txt', probabilities.eval(feed_dict={X: test_set1340.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1341.txt', probabilities.eval(feed_dict={X: test_set1341.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1342.txt', probabilities.eval(feed_dict={X: test_set1342.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1344.txt', probabilities.eval(feed_dict={X: test_set1344.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1345.txt', probabilities.eval(feed_dict={X: test_set1345.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1346.txt', probabilities.eval(feed_dict={X: test_set1346.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1347.txt', probabilities.eval(feed_dict={X: test_set1347.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1348.txt', probabilities.eval(feed_dict={X: test_set1348.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1349.txt', probabilities.eval(feed_dict={X: test_set1349.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1350.txt', probabilities.eval(feed_dict={X: test_set1350.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1351.txt', probabilities.eval(feed_dict={X: test_set1351.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1352.txt', probabilities.eval(feed_dict={X: test_set1352.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1353.txt', probabilities.eval(feed_dict={X: test_set1353.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1354.txt', probabilities.eval(feed_dict={X: test_set1354.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1355.txt', probabilities.eval(feed_dict={X: test_set1355.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1356.txt', probabilities.eval(feed_dict={X: test_set1356.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1357.txt', probabilities.eval(feed_dict={X: test_set1357.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1358.txt', probabilities.eval(feed_dict={X: test_set1358.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1360.txt', probabilities.eval(feed_dict={X: test_set1360.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1362.txt', probabilities.eval(feed_dict={X: test_set1362.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1363.txt', probabilities.eval(feed_dict={X: test_set1363.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1364.txt', probabilities.eval(feed_dict={X: test_set1364.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1366.txt', probabilities.eval(feed_dict={X: test_set1366.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1367.txt', probabilities.eval(feed_dict={X: test_set1367.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1368.txt', probabilities.eval(feed_dict={X: test_set1368.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1369.txt', probabilities.eval(feed_dict={X: test_set1369.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1370.txt', probabilities.eval(feed_dict={X: test_set1370.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1371.txt', probabilities.eval(feed_dict={X: test_set1371.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1372.txt', probabilities.eval(feed_dict={X: test_set1372.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1373.txt', probabilities.eval(feed_dict={X: test_set1373.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1374.txt', probabilities.eval(feed_dict={X: test_set1374.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1376.txt', probabilities.eval(feed_dict={X: test_set1376.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1377.txt', probabilities.eval(feed_dict={X: test_set1377.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1379.txt', probabilities.eval(feed_dict={X: test_set1379.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1380.txt', probabilities.eval(feed_dict={X: test_set1380.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1381.txt', probabilities.eval(feed_dict={X: test_set1381.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1382.txt', probabilities.eval(feed_dict={X: test_set1382.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1384.txt', probabilities.eval(feed_dict={X: test_set1384.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1385.txt', probabilities.eval(feed_dict={X: test_set1385.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1387.txt', probabilities.eval(feed_dict={X: test_set1387.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1390.txt', probabilities.eval(feed_dict={X: test_set1390.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1392.txt', probabilities.eval(feed_dict={X: test_set1392.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1393.txt', probabilities.eval(feed_dict={X: test_set1393.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1394.txt', probabilities.eval(feed_dict={X: test_set1394.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1395.txt', probabilities.eval(feed_dict={X: test_set1395.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1397.txt', probabilities.eval(feed_dict={X: test_set1397.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1403.txt', probabilities.eval(feed_dict={X: test_set1403.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1405.txt', probabilities.eval(feed_dict={X: test_set1405.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1406.txt', probabilities.eval(feed_dict={X: test_set1406.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1408.txt', probabilities.eval(feed_dict={X: test_set1408.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1411.txt', probabilities.eval(feed_dict={X: test_set1411.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1413.txt', probabilities.eval(feed_dict={X: test_set1413.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1414.txt', probabilities.eval(feed_dict={X: test_set1414.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1416.txt', probabilities.eval(feed_dict={X: test_set1416.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1417.txt', probabilities.eval(feed_dict={X: test_set1417.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1418.txt', probabilities.eval(feed_dict={X: test_set1418.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1419.txt', probabilities.eval(feed_dict={X: test_set1419.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1420.txt', probabilities.eval(feed_dict={X: test_set1420.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1421.txt', probabilities.eval(feed_dict={X: test_set1421.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1422.txt', probabilities.eval(feed_dict={X: test_set1422.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1423.txt', probabilities.eval(feed_dict={X: test_set1423.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1424.txt', probabilities.eval(feed_dict={X: test_set1424.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1426.txt', probabilities.eval(feed_dict={X: test_set1426.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1429.txt', probabilities.eval(feed_dict={X: test_set1429.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1430.txt', probabilities.eval(feed_dict={X: test_set1430.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1435.txt', probabilities.eval(feed_dict={X: test_set1435.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1436.txt', probabilities.eval(feed_dict={X: test_set1436.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1438.txt', probabilities.eval(feed_dict={X: test_set1438.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1440.txt', probabilities.eval(feed_dict={X: test_set1440.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1441.txt', probabilities.eval(feed_dict={X: test_set1441.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1442.txt', probabilities.eval(feed_dict={X: test_set1442.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1443.txt', probabilities.eval(feed_dict={X: test_set1443.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1444.txt', probabilities.eval(feed_dict={X: test_set1444.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1445.txt', probabilities.eval(feed_dict={X: test_set1445.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1446.txt', probabilities.eval(feed_dict={X: test_set1446.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1447.txt', probabilities.eval(feed_dict={X: test_set1447.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1448.txt', probabilities.eval(feed_dict={X: test_set1448.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1449.txt', probabilities.eval(feed_dict={X: test_set1449.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1451.txt', probabilities.eval(feed_dict={X: test_set1451.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1454.txt', probabilities.eval(feed_dict={X: test_set1454.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1455.txt', probabilities.eval(feed_dict={X: test_set1455.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1457.txt', probabilities.eval(feed_dict={X: test_set1457.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1459.txt', probabilities.eval(feed_dict={X: test_set1459.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1460.txt', probabilities.eval(feed_dict={X: test_set1460.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1461.txt', probabilities.eval(feed_dict={X: test_set1461.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1462.txt', probabilities.eval(feed_dict={X: test_set1462.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1465.txt', probabilities.eval(feed_dict={X: test_set1465.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1466.txt', probabilities.eval(feed_dict={X: test_set1466.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1467.txt', probabilities.eval(feed_dict={X: test_set1467.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1469.txt', probabilities.eval(feed_dict={X: test_set1469.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1472.txt', probabilities.eval(feed_dict={X: test_set1472.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1474.txt', probabilities.eval(feed_dict={X: test_set1474.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1475.txt', probabilities.eval(feed_dict={X: test_set1475.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1476.txt', probabilities.eval(feed_dict={X: test_set1476.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1477.txt', probabilities.eval(feed_dict={X: test_set1477.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1480.txt', probabilities.eval(feed_dict={X: test_set1480.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1482.txt', probabilities.eval(feed_dict={X: test_set1482.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1483.txt', probabilities.eval(feed_dict={X: test_set1483.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1485.txt', probabilities.eval(feed_dict={X: test_set1485.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1486.txt', probabilities.eval(feed_dict={X: test_set1486.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1488.txt', probabilities.eval(feed_dict={X: test_set1488.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1489.txt', probabilities.eval(feed_dict={X: test_set1489.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1491.txt', probabilities.eval(feed_dict={X: test_set1491.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1494.txt', probabilities.eval(feed_dict={X: test_set1494.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1495.txt', probabilities.eval(feed_dict={X: test_set1495.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1496.txt', probabilities.eval(feed_dict={X: test_set1496.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1497.txt', probabilities.eval(feed_dict={X: test_set1497.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1500.txt', probabilities.eval(feed_dict={X: test_set1500.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1502.txt', probabilities.eval(feed_dict={X: test_set1502.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1503.txt', probabilities.eval(feed_dict={X: test_set1503.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1505.txt', probabilities.eval(feed_dict={X: test_set1505.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1506.txt', probabilities.eval(feed_dict={X: test_set1506.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1507.txt', probabilities.eval(feed_dict={X: test_set1507.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1508.txt', probabilities.eval(feed_dict={X: test_set1508.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1509.txt', probabilities.eval(feed_dict={X: test_set1509.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1512.txt', probabilities.eval(feed_dict={X: test_set1512.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1513.txt', probabilities.eval(feed_dict={X: test_set1513.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1514.txt', probabilities.eval(feed_dict={X: test_set1514.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1515.txt', probabilities.eval(feed_dict={X: test_set1515.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1517.txt', probabilities.eval(feed_dict={X: test_set1517.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1518.txt', probabilities.eval(feed_dict={X: test_set1518.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1522.txt', probabilities.eval(feed_dict={X: test_set1522.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1523.txt', probabilities.eval(feed_dict={X: test_set1523.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1524.txt', probabilities.eval(feed_dict={X: test_set1524.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1526.txt', probabilities.eval(feed_dict={X: test_set1526.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1527.txt', probabilities.eval(feed_dict={X: test_set1527.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
	np.savetxt('result1528.txt', probabilities.eval(feed_dict={X: test_set1528.data, tst: False, pkeep: 1.0, pkeep_conv: 1.0}), delimiter=',')
