# EVA

## What are Channels and Kernels (according to EVA)?
Channels are the feature maps generated when the Kernels convolve over the images. Except the input image we can generate as many channels we want and the number is decided by the number of Kernels doing the convolution operation.
Kernels, Filters, Feature Extracters and 3X3 matrix, all of them are the same. Kernels are use to extract the important features from the images. During the first forward pass kernels are intitialized to get the best possible start and then on the value of numbers in the kernels is taken care by the back-propagation.

## Why should we only (well mostly) use 3x3 Kernels?
3X3 kernels are the most popular and widely used kernels because they have the line of symmetry in them which is necessary to extract all possible features from an image. But, what about other odd number kernels like 5X5 or 7X7, they also have the line of symmetry in them, yes, but after understanding the concept of receptive field researchers realized that what they can achieve from 5X5, 7X7 or 11X11, same can be achieved by using multiple 3X3 size kernels and impact that will be computational efficiency because multiple 3X3 size kernels will have less number of parameters than other odd kernels.

So, this boosted the use of 3X3 kernels and to support the cause further companies like nVidea they made changes in their hardware to support the use of 3X3 futher.

## How many times do we need to perform 3x3 convolution operation to reach 1x1 from 199x199 (show calculations)
199X199|3X3|197X197 197X197|3X3|195X195 195X195|3X3|193X193 193X193|3X3|191X191 191X191|3X3|189X189
189X189|3X3|187X187 187X187|3X3|185X185 185X185|3X3|183X183 183X183|3X3|181X181 181X181|3X3|179X179
179X179|3X3|177X177 177X177|3X3|175X175 175X175|3X3|173X173 173X173|3X3|171X171 171X171|3X3|169X169
169X169|3X3|167X167 167X167|3X3|165X165 165X165|3X3|163X163 163X163|3X3|161X161 161X161|3X3|159X159
159X159|3X3|157X157 157X157|3X3|155X155 155X155|3X3|153X153 153X153|3X3|151X151 151X151|3X3|149X149
149X149|3X3|147X147 147X147|3X3|145X145 145X145|3X3|143X143 143X143|3X3|141X141 141X141|3X3|139X139
139X139|3X3|137X137 137X137|3X3|135X135 135X135|3X3|133X133 133X133|3X3|131X131 131X131|3X3|129X129
129X129|3X3|127X127 127X127|3X3|125X125 125X125|3X3|123X123 123X123|3X3|121X121 121X121|3X3|119X119
119X119|3X3|117X117 117X117|3X3|115X115 115X115|3X3|113X113 113X113|3X3|111X111 111X111|3X3|109X109
109X109|3X3|107X107 107X107|3X3|105X105 105X105|3X3|103X103 103X103|3X3|101X101 101X101|3X3|99X99
99X99|3X3|97X97 97X97|3X3|95X95 95X95|3X3|93X93 93X93|3X3|91X91 91X91|3X3|89X89
89X89|3X3|87X87 87X87|3X3|85X85 85X85|3X3|83X83 83X83|3X3|81X81 81X81|3X3|79X79
79X79|3X3|77X77 77X77|3X3|75X75 75X75|3X3|73X73 73X73|3X3|71X71 71X71|3X3|69X69
69X69|3X3|67X67 67X67|3X3|65X65 65X65|3X3|63X63 63X63|3X3|61X61 61X61|3X3|59X59
59X59|3X3|57X57 57X57|3X3|55X55 55X55|3X3|53X53 53X53|3X3|51X51 51X51|3X3|49X49
49X49|3X3|47X47 47X47|3X3|45X45 45X45|3X3|43X43 43X43|3X3|41X41 41X41|3X3|39X39
39X39|3X3|37X37 37X37|3X3|35X35 35X35|3X3|33X33 33X33|3X3|31X31 31X31|3X3|29X29
29X29|3X3|27X27 27X27|3X3|25X25 25X25|3X3|23X23 23X23|3X3|21X21 21X21|3X3|19X19
19X19|3X3|17X17 17X17|3X3|15X15 15X15|3X3|13X13 13X13|3X3|11X11 11X11|3X3|9X9
9X9|3X3|7X7 7X7|3X3|5X5 5X5|3X3|3X3 3X3|3X3|1X1 
