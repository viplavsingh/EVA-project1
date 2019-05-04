# EVA-project1

1. What are Channels and Kernels?
Ans:
Channels are the combinations of a feature extractor. For instance, in a bowl of biryani, we have several ingredients like rice, peas,
cloves etc. These are the features of the final product. The collection of all the values of a feature is called a channel for that feature. In the example of Biryani, collection of all the peas can be called as a peas channel. So, a image can be composed of many channels.

Kernels are the feature extractor. Kernel is basically a 3x3 matrix and also known as filter. 
Kernels are the 3x3 matrix with values initialised which are then convoled over an image. The image pixel values are multiplied
element wise with the kernel values that are placed above it. The kernel is moved over the whole image horizontally and the vertically by a pixel each time, which is called stride. After applying the convolution, output image is generated which can be edges, patterns, parts of object, objects or scenes based on the layer of convolution we are operating on.


2. Why should we only (well mostly) use 3x3 Kernels?
Ans:
3x3 falls under odd number pixels. Reason for not using even number pixels is it is very dificult to create something which is symmetric
using even number pixels. There is no concept of middle and then we lose on symmetric aspect. 
Now having ruled out the possibility of using even number pixels, we can use odd no of pixels like 3x3, 5x5, 7x7 etc. But we mostly use
3x3. 5x5 can be convoled using two 3x3 kernel and we avoid using so many parameters. So when we use 5x5 kernel in a layer, we use 25 parameters whereas if we use two 3x3 conv layer, we only use 18 parameter and thus we save using lot of parameters. Same goes for 7x7.

Also 3x3 is heavily optimised now and a lot of architectural changes have gone into optimizing for 3x3.


3. How many times do we need to perform 3x3 convolution operation to reach 1x1 from 199x199 (show calculations)
Ans: 99 times
199x199 | (3x3 conv1) |
197x197 | (3x3 conv2) |
195x195 | (3x3 conv3) |
193x193 | (3x3 conv4) |
191x191 | (3x3 conv5) |
189x189 | (3x3 conv6) |
187x187 | (3x3 conv7) |
185x185 | (3x3 conv8) |
183x183 | (3x3 conv9) |
181x181 | (3x3 conv10) |
179x179 | (3x3 conv11) |
177x177 | (3x3 conv12) |
175x175 | (3x3 conv13) |
173x173 | (3x3 conv14) |
171x171 | (3x3 conv15) |
169x169 | (3x3 conv16) |
167x167 | (3x3 conv17) |
165x165 | (3x3 conv18) |
163x163 | (3x3 conv19) |
161x161 | (3x3 conv20) |
159x159 | (3x3 conv21) |
157x157 | (3x3 conv22) |
155x155 | (3x3 conv23) |
153x153 | (3x3 conv24) |
151x151 | (3x3 conv25) |
149x149 | (3x3 conv26) |
147x147 | (3x3 conv27) |
145x145 | (3x3 conv28) |
143x143 | (3x3 conv29) |
141x141 | (3x3 conv30) |
139x139 | (3x3 conv31) |
137x137 | (3x3 conv32) |
135x135 | (3x3 conv33) |
133x133 | (3x3 conv34) |
131x131 | (3x3 conv35) |
129x129 | (3x3 conv36) |
127x127 | (3x3 conv37) |
125x125 | (3x3 conv38) |
123x123 | (3x3 conv39) |
121x121 | (3x3 conv40) |
119x119 | (3x3 conv41) |
117x117 | (3x3 conv42) |
115x115 | (3x3 conv43) |
113x113 | (3x3 conv44) |
111x111 | (3x3 conv45) |
109x109 | (3x3 conv46) |
107x107 | (3x3 conv47) |
105x105 | (3x3 conv48) |
103x103 | (3x3 conv49) |
101x101 | (3x3 conv50) |
99x99 | (3x3 conv51) |
97x97 | (3x3 conv52) |
95x95 | (3x3 conv53) |
93x93 | (3x3 conv54) |
91x91 | (3x3 conv55) |
89x89 | (3x3 conv56) |
87x87 | (3x3 conv57) |
85x85 | (3x3 conv58) |
83x83 | (3x3 conv59) |
81x81 | (3x3 conv60) |
79x79 | (3x3 conv61) |
77x77 | (3x3 conv62) |
75x75 | (3x3 conv63) |
73x73 | (3x3 conv64) |
71x71 | (3x3 conv65) |
69x69 | (3x3 conv66) |
67x67 | (3x3 conv67) |
65x65 | (3x3 conv68) |
63x63 | (3x3 conv69) |
61x61 | (3x3 conv70) |
59x59 | (3x3 conv71) |
57x57 | (3x3 conv72) |
55x55 | (3x3 conv73) |
53x53 | (3x3 conv74) |
51x51 | (3x3 conv75) |
49x49 | (3x3 conv76) |
47x47 | (3x3 conv77) |
45x45 | (3x3 conv78) |
43x43 | (3x3 conv79) |
41x41 | (3x3 conv80) |
39x39 | (3x3 conv81) |
37x37 | (3x3 conv82) |
35x35 | (3x3 conv83) |
33x33 | (3x3 conv84) |
31x31 | (3x3 conv85) |
29x29 | (3x3 conv86) |
27x27 | (3x3 conv87) |
25x25 | (3x3 conv88) |
23x23 | (3x3 conv89) |
21x21 | (3x3 conv90) |
19x19 | (3x3 conv91) |
17x17 | (3x3 conv92) |
15x15 | (3x3 conv93) |
13x13 | (3x3 conv94) |
11x11 | (3x3 conv95) |
9x9 | (3x3 conv96) |
7x7 | (3x3 conv97) |
5x5 | (3x3 conv98) |
3x3 | (3x3 conv99) |
1x1  




