# R_programming_Assignment2
Assignment. Air pollution

> getwd()
[1] "C:/Program Files/R/specdata"
> specdata <- getwd()
> list.files(specdata)
  [1] "001.csv" "002.csv" "003.csv" "004.csv" "005.csv" "006.csv" "007.csv"
  [8] "008.csv" "009.csv" "010.csv" "011.csv" "012.csv" "013.csv" "014.csv"
 [15] "015.csv" "016.csv" "017.csv" "018.csv" "019.csv" "020.csv" "021.csv"
 [22] "022.csv" "023.csv" "024.csv" "025.csv" "026.csv" "027.csv" "028.csv"
 [29] "029.csv" "030.csv" "031.csv" "032.csv" "033.csv" "034.csv" "035.csv"
 [36] "036.csv" "037.csv" "038.csv" "039.csv" "040.csv" "041.csv" "042.csv"
 [43] "043.csv" "044.csv" "045.csv" "046.csv" "047.csv" "048.csv" "049.csv"
 [50] "050.csv" "051.csv" "052.csv" "053.csv" "054.csv" "055.csv" "056.csv"
 [57] "057.csv" "058.csv" "059.csv" "060.csv" "061.csv" "062.csv" "063.csv"
 [64] "064.csv" "065.csv" "066.csv" "067.csv" "068.csv" "069.csv" "070.csv"
 [71] "071.csv" "072.csv" "073.csv" "074.csv" "075.csv" "076.csv" "077.csv"
 [78] "078.csv" "079.csv" "080.csv" "081.csv" "082.csv" "083.csv" "084.csv"
 [85] "085.csv" "086.csv" "087.csv" "088.csv" "089.csv" "090.csv" "091.csv"
 [92] "092.csv" "093.csv" "094.csv" "095.csv" "096.csv" "097.csv" "098.csv"
 [99] "099.csv" "100.csv" "101.csv" "102.csv" "103.csv" "104.csv" "105.csv"
[106] "106.csv" "107.csv" "108.csv" "109.csv" "110.csv" "111.csv" "112.csv"
[113] "113.csv" "114.csv" "115.csv" "116.csv" "117.csv" "118.csv" "119.csv"
[120] "120.csv" "121.csv" "122.csv" "123.csv" "124.csv" "125.csv" "126.csv"
[127] "127.csv" "128.csv" "129.csv" "130.csv" "131.csv" "132.csv" "133.csv"
[134] "134.csv" "135.csv" "136.csv" "137.csv" "138.csv" "139.csv" "140.csv"
[141] "141.csv" "142.csv" "143.csv" "144.csv" "145.csv" "146.csv" "147.csv"
[148] "148.csv" "149.csv" "150.csv" "151.csv" "152.csv" "153.csv" "154.csv"
[155] "155.csv" "156.csv" "157.csv" "158.csv" "159.csv" "160.csv" "161.csv"
[162] "162.csv" "163.csv" "164.csv" "165.csv" "166.csv" "167.csv" "168.csv"
[169] "169.csv" "170.csv" "171.csv" "172.csv" "173.csv" "174.csv" "175.csv"
[176] "176.csv" "177.csv" "178.csv" "179.csv" "180.csv" "181.csv" "182.csv"
[183] "183.csv" "184.csv" "185.csv" "186.csv" "187.csv" "188.csv" "189.csv"
[190] "190.csv" "191.csv" "192.csv" "193.csv" "194.csv" "195.csv" "196.csv"
[197] "197.csv" "198.csv" "199.csv" "200.csv" "201.csv" "202.csv" "203.csv"
[204] "204.csv" "205.csv" "206.csv" "207.csv" "208.csv" "209.csv" "210.csv"
[211] "211.csv" "212.csv" "213.csv" "214.csv" "215.csv" "216.csv" "217.csv"
[218] "218.csv" "219.csv" "220.csv" "221.csv" "222.csv" "223.csv" "224.csv"
[225] "225.csv" "226.csv" "227.csv" "228.csv" "229.csv" "230.csv" "231.csv"
[232] "232.csv" "233.csv" "234.csv" "235.csv" "236.csv" "237.csv" "238.csv"
[239] "239.csv" "240.csv" "241.csv" "242.csv" "243.csv" "244.csv" "245.csv"
[246] "246.csv" "247.csv" "248.csv" "249.csv" "250.csv" "251.csv" "252.csv"
[253] "253.csv" "254.csv" "255.csv" "256.csv" "257.csv" "258.csv" "259.csv"
[260] "260.csv" "261.csv" "262.csv" "263.csv" "264.csv" "265.csv" "266.csv"
[267] "267.csv" "268.csv" "269.csv" "270.csv" "271.csv" "272.csv" "273.csv"
[274] "274.csv" "275.csv" "276.csv" "277.csv" "278.csv" "279.csv" "280.csv"
[281] "281.csv" "282.csv" "283.csv" "284.csv" "285.csv" "286.csv" "287.csv"
[288] "288.csv" "289.csv" "290.csv" "291.csv" "292.csv" "293.csv" "294.csv"
[295] "295.csv" "296.csv" "297.csv" "298.csv" "299.csv" "300.csv" "301.csv"
[302] "302.csv" "303.csv" "304.csv" "305.csv" "306.csv" "307.csv" "308.csv"
[309] "309.csv" "310.csv" "311.csv" "312.csv" "313.csv" "314.csv" "315.csv"
[316] "316.csv" "317.csv" "318.csv" "319.csv" "320.csv" "321.csv" "322.csv"
[323] "323.csv" "324.csv" "325.csv" "326.csv" "327.csv" "328.csv" "329.csv"
[330] "330.csv" "331.csv" "332.csv"
> files <- list.files(specdata)
> directory <- specdata
> files_list <- list.files(directory,full.names=TRUE)
> dat <- data.frame()
> number_of_files <- length(files)
> number_of_files
[1] 332
> for (i in number_of_files) {
+ dat <- rbind(dat, read.csv(files_list[i]))
+ }
> mean(dat[, "sulfate"], na.rm=TRUE)
[1] 1.25
> mean(dat[, "nitrate"], na.rm=TRUE)
[1] 0.1819444
> head(dat)
        Date sulfate nitrate  ID
1 2003-01-01      NA      NA 332
2 2003-01-02      NA      NA 332
3 2003-01-03      NA      NA 332
4 2003-01-04      NA      NA 332
5 2003-01-05      NA      NA 332
6 2003-01-06      NA      NA 332
> pollutantmean <- function(directory, pollutant, id = 1:332) {
+ dat <- data.frame()
+ files_list <- list.files(directory, full.names=TRUE)
+ for (i in id) {
+ dat <- rbind(dat, read.csv(files_list[i]))
+ }
+ mean(dat[, pollutant], na.rm=TRUE)
+ }
> pollutantmean(specdata, "sulfate", id=1:5)
[1] 4.321342
> pollutantmean(specdata, "nitrate", id=1:5)
[1] 0.9030249
> pollutantmean(specdata, "sulfate", id=1:10)
[1] 4.064128
> pollutantmean(specdata, "nitrate", id=1:10)
[1] 0.7976266
> pollutantmean(specdata, "nitrate", id=70:72)
[1] 1.706047
> pollutantmean(specdata, "nitrate", id=23)
[1] 1.280833
> source("http://d396qusza40orc.cloudfront.net/rprog%2Fscripts%2Fsubmitscript1.R")
> submit()

Press Enter to continue...

| The first item I need is your Course ID. For example, if the homepage for
| your Coursera course was 'https://class.coursera.org/rprog-001', then your
| course ID would be 'rprog-001' (without the quotes).

Course ID: rprog-001

| It looks like you entered the Course ID that I used as an example, which is
| not what I'm looking for.

| Instead, I need your Course ID, which is the last part of the web address for
| your Coursera course. For example, if the homepage for your Coursera course
| was 'https://class.coursera.org/rprog-001', then your course ID would be
| 'rprog-001' (without the quotes).

Course ID: rprog-012
Submission login (email): esther_muchai@yahoo.com
Submission  password: dZ2kSXqZf8

| Is the following information correct?

Course ID: rprog-012
Submission login (email): esther_muchai@yahoo.com
Submission password: dZ2kSXqZf8

1: Yes, go ahead!
2: No, I need to change something.

Selection: 1

| Which part are you submitting?

 1: 'pollutantmean' part 1
 2: 'pollutantmean' part 2
 3: 'pollutantmean' part 3
 4: 'pollutantmean' part 4
 5: 'complete' part 1
 6: 'complete' part 2
 7: 'complete' part 3
 8: 'corr' part 1
 9: 'corr' part 2
10: 'corr' part 3

Selection: 1,2,3,4
Error in source("pollutantmean.R") : 
  pollutantmean.R:2:3: unexpected symbol
1: 
2: R version


> pollutantmean(specdata, "sulfate", id=1:10)
[1] 4.064128

> pollutantmean(specdata, "nitrate", id=70:72)
[1] 1.706047
> pollutantmean(specdata, "nitrate", id=23)
[1] 1.280833
