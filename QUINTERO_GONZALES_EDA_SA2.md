sa2_EDA
================
QUINTERO & GONZALES
2025-05-19

``` r
# importing and loading csv file

maleresp <- read.csv("C:/Users/sbcvj/Downloads/male_respondents.csv")
head(maleresp)
```

    ##   CaseID RSCRAGE RSCRNINF RSCRHISP RSCRRACE FTFMODE    DEVICE_TYPE AGE_R
    ## 1  96063      27        1        1        4       2             PC    27
    ## 2  96065      31        1        1        4       2         Mobile    31
    ## 3  96067      37        1        5        3       1 Not applicable    37
    ## 4  96069      39        5        5        3       2         Mobile    40
    ## 5  96070      17        5        1        4       1 Not applicable    17
    ## 6  96073      15        5        5        3       1 Not applicable    15
    ##   AGESCRN HISP HISPGRP ROSCNT HHKIDS18 NONBIOKIDS MARSTAT LMARSTAT RMARIT
    ## 1      27    1       1      3        0          0       3        6      0
    ## 2      31    1       2      2        0          0       1       NA      1
    ## 3      37    5      NA      8        4          0       1       NA      1
    ## 4      39    5      NA      3        1          0       1       NA      1
    ## 5      17    1       2      4        0          0       3        6      0
    ## 6      15    5      NA      3        0          0       3        6      0
    ##   EVRMARRY SSMARCOH WOMREL EARNHS_Y MYSCHOL_Y EARNBA_Y WTHPARNW ONOWN ONOWN18
    ## 1        0        0     NA     2013        NA       NA        1     5       5
    ## 2        1        0     NA     2009        NA       NA        2     5       5
    ## 3        1        0      1       NA        NA       NA        2     5       5
    ## 4        1        0      1     2002        NA     2006        2     5       5
    ## 5        0        0     NA       NA      2022       NA        1     5       5
    ## 6        0        0     NA       NA      2023       NA        2     5       5
    ##   INTACT PARMARR INTACT18 LVSIT14F LVSIT14M WOMRASDU MOMWORKD MANRASDU FOSTEREV
    ## 1      1       1        1       NA       NA       NA        1       NA        5
    ## 2      1       1        1       NA       NA       NA        1       NA        5
    ## 3      1       1        1       NA       NA       NA        4       NA        5
    ## 4      1       1        1       NA       NA       NA        1       NA        5
    ## 5      1       1        1       NA       NA       NA        2       NA        5
    ## 6     NA       5        2        1        3        1        2        1        1
    ##   MNYFSTER DURFSTER AGEFSTER EVCOHAB1 NUMCOH1 EVCOHAB2 NUMCOH2 EVRCOHAB
    ## 1       NA       NA       NA       NA      NA        5      NA        0
    ## 2       NA       NA       NA        5      NA       NA      NA        0
    ## 3       NA       NA       NA        5      NA       NA      NA        0
    ## 4       NA       NA       NA        5      NA       NA      NA        0
    ## 5       NA       NA       NA       NA      NA        5      NA        0
    ## 6        2        1        2       NA      NA        5      NA        0
    ##   NUMCOHAB MARSTATB EVCOHABB NUMCOHB FMARIT EVERSEX RHADSEX YNOSEX TALKPAR1
    ## 1       NA       NA       NA      NA      5       5       2      4       NA
    ## 2       NA       NA       NA      NA      1      NA       1     NA       NA
    ## 3       NA       NA       NA      NA      1      NA       1     NA       NA
    ## 4       NA       NA       NA      NA      1      NA       1     NA       NA
    ## 5       NA       NA       NA      NA      5       1       1     NA        1
    ## 6       NA       NA       NA      NA      5       1       1     NA        1
    ##   TALKPAR2 TALKPAR3 TALKPAR4 TALKPAR5 TALKPAR6 TALKPAR7 SEDNO SEDNOLC1 SEDNOLC2
    ## 1       NA       NA       NA       NA       NA       NA    NA       NA       NA
    ## 2       NA       NA       NA       NA       NA       NA    NA       NA       NA
    ## 3       NA       NA       NA       NA       NA       NA    NA       NA       NA
    ## 4       NA       NA       NA       NA       NA       NA    NA       NA       NA
    ## 5        2        4        5        6        7       NA     1        1       NA
    ## 6        2        3        4        5        6        7     1        1       NA
    ##   SEDNOLC3 SEDNOLC4 SEDNOG SEDNOSX SEDBC SEDBCLC1 SEDBCLC2 SEDBCLC3 SEDBCLC4
    ## 1       NA       NA     NA      NA    NA       NA       NA       NA       NA
    ## 2       NA       NA     NA      NA    NA       NA       NA       NA       NA
    ## 3       NA       NA     NA      NA    NA       NA       NA       NA       NA
    ## 4       NA       NA     NA      NA    NA       NA       NA       NA       NA
    ## 5       NA       NA      7       1     1        1       NA       NA       NA
    ## 6       NA       NA      8       1     1        1       NA       NA       NA
    ##   SEDBCG SEDBCSX SEDWHBC SEDWHLC1 SEDWHLC2 SEDWHLC3 SEDWHLC4 SEDWHBCG SEDWBCSX
    ## 1     NA      NA      NA       NA       NA       NA       NA       NA       NA
    ## 2     NA      NA      NA       NA       NA       NA       NA       NA       NA
    ## 3     NA      NA      NA       NA       NA       NA       NA       NA       NA
    ## 4     NA      NA      NA       NA       NA       NA       NA       NA       NA
    ## 5      7       1       5       NA       NA       NA       NA       NA       NA
    ## 6      8       1       1        1       NA       NA       NA        8        1
    ##   SEDCOND SEDCONLC1 SEDCONLC2 SEDCONLC3 SEDCONLC4 SEDCONDG SEDCONSX SEDSTD
    ## 1      NA        NA        NA        NA        NA       NA       NA     NA
    ## 2      NA        NA        NA        NA        NA       NA       NA     NA
    ## 3      NA        NA        NA        NA        NA       NA       NA     NA
    ## 4      NA        NA        NA        NA        NA       NA       NA     NA
    ## 5       1         9        NA        NA        NA        8        1      1
    ## 6       1         1        NA        NA        NA        8        1      1
    ##   SEDSTDLC1 SEDSTDLC2 SEDSTDLC3 SEDSTDLC4 SEDSTDG SEDSTDSX SEDHIV SEDHIVLC1
    ## 1        NA        NA        NA        NA      NA       NA     NA        NA
    ## 2        NA        NA        NA        NA      NA       NA     NA        NA
    ## 3        NA        NA        NA        NA      NA       NA     NA        NA
    ## 4        NA        NA        NA        NA      NA       NA     NA        NA
    ## 5         1        NA        NA        NA       8        1      1         1
    ## 6         1        NA        NA        NA       8        1      1         1
    ##   SEDHIVLC2 SEDHIVLC3 SEDHIVLC4 SEDHIVG SEDHIVSX SEDABST SEDABLC1 SEDABLC2
    ## 1        NA        NA        NA      NA       NA      NA       NA       NA
    ## 2        NA        NA        NA      NA       NA      NA       NA       NA
    ## 3        NA        NA        NA      NA       NA      NA       NA       NA
    ## 4        NA        NA        NA      NA       NA      NA       NA       NA
    ## 5        NA        NA        NA       8        1       1        1       NA
    ## 6        NA        NA        NA       8        1       1        1       NA
    ##   SEDABLC3 SEDABLC4 SEDABSTG SEDABSSX EVEROPER TYPEOPER VASEC_Y PLCSTROP
    ## 1       NA       NA       NA       NA        5       NA      NA       NA
    ## 2       NA       NA       NA       NA        5       NA      NA       NA
    ## 3       NA       NA       NA       NA        5       NA      NA       NA
    ## 4       NA       NA       NA       NA        5       NA      NA       NA
    ## 5       NA       NA        7        1        5       NA      NA       NA
    ## 6       NA       NA        8        1        5       NA      NA       NA
    ##   RVRSVAS VASREV_Y RSURGSTR FATHPOSS FATHDIFF RSTRSTAT SXMON12 SEXSTAT
    ## 1      NA       NA        0        1        5        0      NA       0
    ## 2      NA       NA        0        1        9        0      NA       6
    ## 3      NA       NA        0        1        5        0       1       2
    ## 4      NA       NA        0        1        5        0      NA       6
    ## 5      NA       NA        0        1        5        0      NA       6
    ## 6      NA       NA        0        1        5        0       5       3
    ##   P12MOCONO P12MOCON SEXFREQ CONFREQ P1RLTN1 P1CURRWIFE P1CURRSEP P1RLTN2
    ## 1        NA       NA      NA      NA      NA         NA        NA      NA
    ## 2        NA        1       2       2       1          1        NA      NA
    ## 3        NA        5       6       0       1          1        NA      NA
    ## 4        NA        1       6       6       1          1        NA      NA
    ## 5        NA        5       1       0      NA         NA        NA      NA
    ## 6        NA       NA      NA      NA      NA         NA        NA      NA
    ##   P1COHABIT P1SXLAST_M P1SXLAST_Y CMLSXP1 P2RLTN1 P2CURRWIFE P2CURRSEP P2RLTN2
    ## 1        NA         NA         NA      NA      NA         NA        NA      NA
    ## 2        NA          2       2023    1478      NA         NA        NA      NA
    ## 3        NA         10       2022    1474      NA         NA        NA      NA
    ## 4        NA          8       2023    1484      NA         NA        NA      NA
    ## 5        NA          9       2022    1473      NA         NA        NA      NA
    ## 6        NA         11       2020    1451      NA         NA        NA      NA
    ##   P2COHABIT P2SXLAST_M P2SXLAST_Y CMLSXP2 P3RLTN1 P3CURRWIFE P3CURRSEP P3RLTN2
    ## 1        NA         NA         NA      NA      NA         NA        NA      NA
    ## 2        NA         NA         NA      NA      NA         NA        NA      NA
    ## 3        NA         NA         NA      NA      NA         NA        NA      NA
    ## 4        NA         NA         NA      NA      NA         NA        NA      NA
    ## 5        NA         11       2021    1463      NA         NA        NA      NA
    ## 6        NA         NA         NA      NA      NA         NA        NA      NA
    ##   P3COHABIT P3SXLAST_M P3SXLAST_Y CMLSXP3 P1RELATION P2RELATION P3RELATION
    ## 1        NA         NA         NA      NA         NA         NA         NA
    ## 2        NA         NA         NA      NA          1         NA         NA
    ## 3        NA         NA         NA      NA          1         NA         NA
    ## 4        NA         NA         NA      NA          1         NA         NA
    ## 5        NA         NA         NA      NA          6          6         NA
    ## 6        NA         NA         NA      NA          6         NA         NA
    ##   FIRST MARRDATE_Y HISAGEM LIVTOGSP STRTSPCP_Y HISAGEC CMSTRTSP ENGATHEN
    ## 1    NA         NA      NA       NA         NA      NA       NA       NA
    ## 2    NA       2022      30        1       2021      29     2021        5
    ## 3    NA       2005      20        5         NA      NA     2005       NA
    ## 4    NA       2010      26        5         NA      NA     2010       NA
    ## 5    NA         NA      NA       NA         NA      NA       NA       NA
    ## 6    NA         NA      NA       NA         NA      NA       NA       NA
    ##   WILLMARR CSPAGE CSPEDUCN CSPBORN CSPMARBF SSKIDTOG NSSKIDTOG SSKIDTOG18
    ## 1       NA     NA       NA      NA       NA       NA        NA         NA
    ## 2       NA      4        4       1        1       NA        NA         NA
    ## 3       NA      5        1       5        5       NA        NA         NA
    ## 4       NA      5        6       5        5       NA        NA         NA
    ## 5       NA     NA       NA      NA       NA       NA        NA         NA
    ## 6       NA     NA       NA      NA       NA       NA        NA         NA
    ##   CWPSX1WN_M CWPSX1WN_Y CMFSXCWP CWPSX1AG AGEFSXCWP CWPSX1RL CWPFUSE CWPFMET01
    ## 1         NA         NA       NA       NA        NA       NA      NA        NA
    ## 2          1       2019     1429       NA        27        6       1         1
    ## 3         10       2005     1270       NA        20        1       5        NA
    ## 4          9       2003     1245       NA        20        8       1         1
    ## 5         NA         NA       NA       NA        NA       NA      NA        NA
    ## 6         NA         NA       NA       NA        NA       NA      NA        NA
    ##   CWPFMET02 CWPFMET03 CWPFMET04 CWPFMET05 CWPOPSTR CWPREVST PSURGSTR CWPPOSS
    ## 1        NA        NA        NA        NA       NA       NA       NA      NA
    ## 2        NA        NA        NA        NA        5       NA        0       1
    ## 3        NA        NA        NA        NA        5       NA        0       1
    ## 4        12        NA        NA        NA        5       NA        0       1
    ## 5        NA        NA        NA        NA       NA       NA       NA      NA
    ## 6        NA        NA        NA        NA       NA       NA       NA      NA
    ##   CWPDIFF PSTRSTAT CWPLSXWN_M CWPLSXWN_Y CMLSXCWP CWPLUSE1 CWPLMET11 CWPLMET12
    ## 1      NA       NA         NA         NA       NA       NA        NA        NA
    ## 2       5        0         NA         NA     1478        1         1        NA
    ## 3       5        0         NA         NA     1474        5        NA        NA
    ## 4       5        0         NA         NA     1484        1         1        NA
    ## 5      NA       NA         NA         NA       NA       NA        NA        NA
    ## 6      NA       NA         NA         NA       NA       NA        NA        NA
    ##   CWPLMET13 CWPLMET14 CWPLUSE2 DKCWPLUSE CWPLMET201 CWPLMET202 CWPLMET203
    ## 1        NA        NA       NA        NA         NA         NA         NA
    ## 2        NA        NA        5        NA         NA         NA         NA
    ## 3        NA        NA        5        NA         NA         NA         NA
    ## 4        NA        NA        1        NA          4         NA         NA
    ## 5        NA        NA       NA        NA         NA         NA         NA
    ## 6        NA        NA       NA        NA         NA         NA         NA
    ##   CWPLSXUSE CWPRECBC CWPALLBC01 CWPALLBC02 CWPALLBC03 CWPALLBC04 CWPALLBC05
    ## 1        NA       NA         NA         NA         NA         NA         NA
    ## 2         1       NA          1         NA         NA         NA         NA
    ## 3         0        5         NA         NA         NA         NA         NA
    ## 4         1       NA          1          4         NA         NA         NA
    ## 5        NA       NA         NA         NA         NA         NA         NA
    ## 6        NA       NA         NA         NA         NA         NA         NA
    ##   CWPBCMST CONDFREQ CWPNOFRQ CWPPRGNW CWPTRYPG CWPTRYLG CWPCPWNT CWPCPSON
    ## 1       NA       NA       NA       NA       NA       NA       NA       NA
    ## 2       NA       40        1        5        5       NA       NA       NA
    ## 3       NA       NA       NA        5        5       NA       NA       NA
    ## 4        1      100       NA        5        5       NA       NA       NA
    ## 5       NA       NA       NA       NA       NA       NA       NA       NA
    ## 6       NA       NA       NA       NA       NA       NA       NA       NA
    ##   CWPCPSNN CWPCPSNMY CWPCPHPY MARDATEN_Y_1 AGEMARR_1 LIVTOGN_1 AGELIV_1
    ## 1       NA        NA       NA           NA        NA        NA       NA
    ## 2       NA        NA       NA           NA        NA        NA       NA
    ## 3       NA        NA       NA           NA        NA        NA       NA
    ## 4       NA        NA       NA           NA        NA        NA       NA
    ## 5       NA        NA       NA           NA        NA        NA       NA
    ## 6       NA        NA       NA           NA        NA        NA       NA
    ##   CMUNIONP_1 ENGAGTHN_1 MARREND_1 ENDMARR_Y_1 STOPLIVE_Y_1 PXCURR PXCURRPRT
    ## 1         NA         NA        NA          NA           NA     NA        NA
    ## 2         NA         NA        NA          NA           NA     NA        NA
    ## 3         NA         NA        NA          NA           NA     NA        NA
    ## 4         NA         NA        NA          NA           NA     NA        NA
    ## 5         NA         NA        NA          NA           NA      5         0
    ## 6         NA         NA        NA          NA           NA     NA         0
    ##   PXMARRY PXLRUSE PXLRMETH1 PXLRMETH2 PXLRMETH3 PXLRMETH4 PXLPUSE DKPXLPUSE
    ## 1      NA      NA        NA        NA        NA        NA      NA        NA
    ## 2      NA      NA        NA        NA        NA        NA      NA        NA
    ## 3      NA      NA        NA        NA        NA        NA      NA        NA
    ## 4      NA      NA        NA        NA        NA        NA      NA        NA
    ## 5      NA       5        NA        NA        NA        NA       5        NA
    ## 6      NA       1         1        NA        NA        NA       5        NA
    ##   PXLPMETH01 PXLPMETH02 PXLPMETH03 PXLPMETH04 PXLPMETH05 LSXUSEP MTONCEP
    ## 1         NA         NA         NA         NA         NA      NA      NA
    ## 2         NA         NA         NA         NA         NA      NA      NA
    ## 3         NA         NA         NA         NA         NA      NA      NA
    ## 4         NA         NA         NA         NA         NA      NA      NA
    ## 5         NA         NA         NA         NA         NA       0       2
    ## 6         NA         NA         NA         NA         NA       1       2
    ##   PXMTONCE PXFRLTN1 PXEDUC PXMARBF PXABLECH PXSXFRST_M PXSXFRST_Y CMFSXP
    ## 1       NA       NA     NA      NA       NA         NA         NA     NA
    ## 2       NA       NA     NA      NA       NA         NA         NA     NA
    ## 3       NA       NA     NA      NA       NA         NA         NA     NA
    ## 4       NA       NA     NA      NA       NA         NA         NA     NA
    ## 5        5        8      1       5       NA         NA         NA     NA
    ## 6       NA        6      1       5       NA         NA         NA     NA
    ##   AGEFSXP PXAGFRST PXFRLTN2 PXFUSE PXFMETH01 PXFMETH02 PXFMETH03 PXFMETH04
    ## 1               NA       NA     NA        NA        NA        NA        NA
    ## 2               NA       NA     NA        NA        NA        NA        NA
    ## 3               NA       NA     NA        NA        NA        NA        NA
    ## 4               NA       NA     NA        NA        NA        NA        NA
    ## 5               NA       NA     NA        NA        NA        NA        NA
    ## 6               NA       NA     NA        NA        NA        NA        NA
    ##   PXFMETH05 PXANYUSE PXMETHOD01 PXMETHOD02 PXMETHOD03 PXMETHOD04 PXMETHOD05
    ## 1        NA       NA         NA         NA         NA         NA         NA
    ## 2        NA       NA         NA         NA         NA         NA         NA
    ## 3        NA       NA         NA         NA         NA         NA         NA
    ## 4        NA       NA         NA         NA         NA         NA         NA
    ## 5        NA       NA         NA         NA         NA         NA         NA
    ## 6        NA       NA         NA         NA         NA         NA         NA
    ##   PXMSTUSE PXCONFRQ PXNOFREQ PXCPREG PXTRYING PXTRYLONG PXRWANT PXRSOON
    ## 1       NA       NA       NA      NA       NA        NA      NA      NA
    ## 2       NA       NA       NA      NA       NA        NA      NA      NA
    ## 3       NA       NA       NA      NA       NA        NA      NA      NA
    ## 4       NA       NA       NA      NA       NA        NA      NA      NA
    ## 5       NA       NA       NA      NA       NA        NA      NA      NA
    ## 6       NA       NA       NA      NA       NA        NA      NA      NA
    ##   PXRSOONN PXRSOONMY PXCPFEEL MARDATEN_Y_2 AGEMARR_2 LIVTOGN_2 AGELIV_2
    ## 1       NA        NA       NA           NA        NA        NA       NA
    ## 2       NA        NA       NA           NA        NA        NA       NA
    ## 3       NA        NA       NA           NA        NA        NA       NA
    ## 4       NA        NA       NA           NA        NA        NA       NA
    ## 5       NA        NA       NA           NA        NA        NA       NA
    ## 6       NA        NA       NA           NA        NA        NA       NA
    ##   CMUNIONP_2 ENGAGTHN_2 MARREND_2 ENDMARR_Y_2 STOPLIVE_Y_2 PXCURR2 PXCURRPRT2
    ## 1         NA         NA        NA          NA           NA      NA         NA
    ## 2         NA         NA        NA          NA           NA      NA         NA
    ## 3         NA         NA        NA          NA           NA      NA         NA
    ## 4         NA         NA        NA          NA           NA      NA         NA
    ## 5         NA         NA        NA          NA           NA       5          0
    ## 6         NA         NA        NA          NA           NA      NA         NA
    ##   PXMARRY2 PXLRUSE2 PXLRMETH5 PXLRMETH6 PXLRMETH7 PXLRMETH8 PXLPUSE2 DKPXLPUSE2
    ## 1       NA       NA        NA        NA        NA        NA       NA         NA
    ## 2       NA       NA        NA        NA        NA        NA       NA         NA
    ## 3       NA       NA        NA        NA        NA        NA       NA         NA
    ## 4       NA       NA        NA        NA        NA        NA       NA         NA
    ## 5       NA        5        NA        NA        NA        NA        5         NA
    ## 6       NA       NA        NA        NA        NA        NA       NA         NA
    ##   PXLPMETH11 PXLPMETH12 PXLPMETH13 PXLPMETH14 PXLPMETH15 LSXUSEP2 MTONCEP2
    ## 1         NA         NA         NA         NA         NA       NA       NA
    ## 2         NA         NA         NA         NA         NA       NA       NA
    ## 3         NA         NA         NA         NA         NA       NA       NA
    ## 4         NA         NA         NA         NA         NA       NA       NA
    ## 5         NA         NA         NA         NA         NA        0        1
    ## 6         NA         NA         NA         NA         NA       NA       NA
    ##   PXMTONCE2 PXFRLTN3 PXEDUC2 PXMARBF2 PXABLECH2 PXSXFRST_M2 PXSXFRST_Y2 CMFSXP2
    ## 1        NA       NA      NA       NA        NA          NA          NA      NA
    ## 2        NA       NA      NA       NA        NA          NA          NA      NA
    ## 3        NA       NA      NA       NA        NA          NA          NA      NA
    ## 4        NA       NA      NA       NA        NA          NA          NA      NA
    ## 5         1        6      NA       NA        NA          11        2021    1463
    ## 6        NA       NA      NA       NA        NA          NA          NA      NA
    ##   AGEFSXP2 PXAGFRST2 PXFRLTN4 PXFUSE2 PXFMETH14 PXFMETH15 PXFMETH16 PXFMETH17
    ## 1       NA        NA       NA      NA        NA        NA        NA        NA
    ## 2       NA        NA       NA      NA        NA        NA        NA        NA
    ## 3       NA        NA       NA      NA        NA        NA        NA        NA
    ## 4       NA        NA       NA      NA        NA        NA        NA        NA
    ## 5       16        NA        6       5        NA        NA        NA        NA
    ## 6       NA        NA       NA      NA        NA        NA        NA        NA
    ##   PXFMETH18 PXANYUSE2 PXMETHOD14 PXMETHOD15 PXMETHOD16 PXMETHOD17 PXMETHOD18
    ## 1        NA        NA         NA         NA         NA         NA         NA
    ## 2        NA        NA         NA         NA         NA         NA         NA
    ## 3        NA        NA         NA         NA         NA         NA         NA
    ## 4        NA        NA         NA         NA         NA         NA         NA
    ## 5        NA        NA         NA         NA         NA         NA         NA
    ## 6        NA        NA         NA         NA         NA         NA         NA
    ##   PXMSTUSE2 PXCONFRQ2 PXNOFREQ2 PXCPREG2 PXTRYING2 PXTRYLONG2 PXRWANT2 PXRSOON2
    ## 1        NA        NA        NA       NA        NA         NA       NA       NA
    ## 2        NA        NA        NA       NA        NA         NA       NA       NA
    ## 3        NA        NA        NA       NA        NA         NA       NA       NA
    ## 4        NA        NA        NA       NA        NA         NA       NA       NA
    ## 5        NA         0         5       NA        NA         NA       NA       NA
    ## 6        NA        NA        NA       NA        NA         NA       NA       NA
    ##   PXRSOONN2 PXRSOONMY2 PXCPFEEL2 MARDATEN_Y_3 AGEMARR_3 LIVTOGN_3 AGELIV_3
    ## 1        NA         NA        NA           NA        NA        NA       NA
    ## 2        NA         NA        NA           NA        NA        NA       NA
    ## 3        NA         NA        NA           NA        NA        NA       NA
    ## 4        NA         NA        NA           NA        NA        NA       NA
    ## 5        NA         NA        NA           NA        NA        NA       NA
    ## 6        NA         NA        NA           NA        NA        NA       NA
    ##   CMUNIONP_3 ENGAGTHN_3 MARREND_3 ENDMARR_Y_3 STOPLIVE_Y_3 PXCURR3 PXCURRPRT3
    ## 1         NA         NA        NA          NA           NA      NA         NA
    ## 2         NA         NA        NA          NA           NA      NA         NA
    ## 3         NA         NA        NA          NA           NA      NA         NA
    ## 4         NA         NA        NA          NA           NA      NA         NA
    ## 5         NA         NA        NA          NA           NA      NA         NA
    ## 6         NA         NA        NA          NA           NA      NA         NA
    ##   PXMARRY3 PXLRUSE3 PXLRMETH9 PXLRMETH10 PXLRMETH11 PXLRMETH12 PXLPUSE3
    ## 1       NA       NA        NA         NA         NA         NA       NA
    ## 2       NA       NA        NA         NA         NA         NA       NA
    ## 3       NA       NA        NA         NA         NA         NA       NA
    ## 4       NA       NA        NA         NA         NA         NA       NA
    ## 5       NA       NA        NA         NA         NA         NA       NA
    ## 6       NA       NA        NA         NA         NA         NA       NA
    ##   DKPXLPUSE3 PXLPMETH21 PXLPMETH22 PXLPMETH23 PXLPMETH24 PXLPMETH25 LSXUSEP3
    ## 1         NA         NA         NA         NA         NA         NA       NA
    ## 2         NA         NA         NA         NA         NA         NA       NA
    ## 3         NA         NA         NA         NA         NA         NA       NA
    ## 4         NA         NA         NA         NA         NA         NA       NA
    ## 5         NA         NA         NA         NA         NA         NA       NA
    ## 6         NA         NA         NA         NA         NA         NA       NA
    ##   MTONCEP3 PXMTONCE3 PXFRLTN5 PXEDUC3 PXMARBF3 PXABLECH3 PXSXFRST_M3
    ## 1       NA        NA       NA      NA       NA        NA          NA
    ## 2       NA        NA       NA      NA       NA        NA          NA
    ## 3       NA        NA       NA      NA       NA        NA          NA
    ## 4       NA        NA       NA      NA       NA        NA          NA
    ## 5       NA        NA       NA      NA       NA        NA          NA
    ## 6       NA        NA       NA      NA       NA        NA          NA
    ##   PXSXFRST_Y3 CMFSXP3 AGEFSXP3 PXAGFRST3 PXFRLTN6 PXFUSE3 PXFMETH27 PXFMETH28
    ## 1          NA      NA       NA        NA       NA      NA        NA        NA
    ## 2          NA      NA       NA        NA       NA      NA        NA        NA
    ## 3          NA      NA       NA        NA       NA      NA        NA        NA
    ## 4          NA      NA       NA        NA       NA      NA        NA        NA
    ## 5          NA      NA       NA        NA       NA      NA        NA        NA
    ## 6          NA      NA       NA        NA       NA      NA        NA        NA
    ##   PXFMETH29 PXFMETH30 PXFMETH31 PXANYUSE3 PXMETHOD27 PXMETHOD28 PXMETHOD29
    ## 1        NA        NA        NA        NA         NA         NA         NA
    ## 2        NA        NA        NA        NA         NA         NA         NA
    ## 3        NA        NA        NA        NA         NA         NA         NA
    ## 4        NA        NA        NA        NA         NA         NA         NA
    ## 5        NA        NA        NA        NA         NA         NA         NA
    ## 6        NA        NA        NA        NA         NA         NA         NA
    ##   PXMETHOD30 PXMETHOD31 PXMSTUSE3 PXCONFRQ3 PXNOFREQ3 PXCPREG3 PXTRYING3
    ## 1         NA         NA        NA        NA        NA       NA        NA
    ## 2         NA         NA        NA        NA        NA       NA        NA
    ## 3         NA         NA        NA        NA        NA       NA        NA
    ## 4         NA         NA        NA        NA        NA       NA        NA
    ## 5         NA         NA        NA        NA        NA       NA        NA
    ## 6         NA         NA        NA        NA        NA       NA        NA
    ##   PXTRYLONG3 PXRWANT3 PXRSOON3 PXRSOONN3 PXRSOONMY3 PXCPFEEL3 CURRPREG CURRPRTS
    ## 1         NA       NA       NA        NA         NA        NA        0        0
    ## 2         NA       NA       NA        NA         NA        NA        0        0
    ## 3         NA       NA       NA        NA         NA        NA        0        0
    ## 4         NA       NA       NA        NA         NA        NA        0        0
    ## 5         NA       NA       NA        NA         NA        NA        0        0
    ## 6         NA       NA       NA        NA         NA        NA        0        0
    ##   NFORMCOHAB FW1MARBEG_Y FW1MARAGE LIVTOGN_W1 AGELIV_W1 CMUNIONW1 ENGAGTHN_W1
    ## 1          0          NA        NA         NA        NA        NA          NA
    ## 2          0        2018        26          5        NA      2018          NA
    ## 3          0          NA        NA         NA        NA        NA          NA
    ## 4          0          NA        NA         NA        NA        NA          NA
    ## 5          0          NA        NA         NA        NA        NA          NA
    ## 6          0          NA        NA         NA        NA        NA          NA
    ##   MARREND_W1 FW1MAREND_Y STOPLIVE_Y_W1 FWPEDUC_W1 FWPMARBF_W1 STRTLIVE_Y_FC1
    ## 1         NA          NA            NA         NA          NA             NA
    ## 2          4          NA          2018          5           5             NA
    ## 3         NA          NA            NA         NA          NA             NA
    ## 4         NA          NA            NA         NA          NA             NA
    ## 5         NA          NA            NA         NA          NA             NA
    ## 6         NA          NA            NA         NA          NA             NA
    ##   AGELIV_FC1 ENGAGTHN_FC1 STOPLIVE_Y_FC1 FWPEDUC_FC1 FWPMARBF_FC1 FPPROBE
    ## 1         NA           NA             NA          NA           NA      NA
    ## 2         NA           NA             NA          NA           NA       1
    ## 3         NA           NA             NA          NA           NA      NA
    ## 4         NA           NA             NA          NA           NA      NA
    ## 5         NA           NA             NA          NA           NA       5
    ## 6         NA           NA             NA          NA           NA      NA
    ##   EVBIOKID NUMBIOKID ONEMOM MOMWHO BCMOMWHO_01 BCMOMAGE_01 BCSEX_01
    ## 1       NA        NA     NA     NA          NA          NA       NA
    ## 2        5        NA     NA     NA          NA          NA       NA
    ## 3        1        10      1      1          NA           2        2
    ## 4        1         1     NA      1          NA           4        1
    ## 5        5        NA     NA     NA          NA          NA       NA
    ## 6        5        NA     NA     NA          NA          NA       NA
    ##   YRBIOCHILD_01 BCAGE_01 BCAGEGRP_01 BCMARLIV_01 BCLRNPRG_01 LIVEHERE_01
    ## 1            NA       NA          NA          NA          NA          NA
    ## 2            NA       NA          NA          NA          NA          NA
    ## 3          2006       16          NA           1          NA           1
    ## 4          2016        7          NA           1          NA          NA
    ## 5            NA       NA          NA          NA          NA          NA
    ## 6            NA       NA          NA          NA          NA          NA
    ##   ALIVENOW_01 BCNOWLIV_01 BCRES_01 BCSIGNBC_01 BCCOURT_01 BCGENTST_01
    ## 1          NA          NA       NA          NA         NA          NA
    ## 2          NA          NA       NA          NA         NA          NA
    ## 3          NA          NA        0          NA         NA          NA
    ## 4          NA          NA        0          NA         NA          NA
    ## 5          NA          NA       NA          NA         NA          NA
    ## 6          NA          NA       NA          NA         NA          NA
    ##   LIVCHEVR_01 BCWANT_01 BCTIMING_01 BCSOONN_01 BCSOONNMY_01 BCHPY_01
    ## 1          NA        NA          NA         NA           NA       NA
    ## 2          NA        NA          NA         NA           NA       NA
    ## 3          NA        NA          NA         NA           NA       NA
    ## 4          NA        NA          NA         NA           NA       NA
    ## 5          NA        NA          NA         NA           NA       NA
    ## 6          NA        NA          NA         NA           NA       NA
    ##   BCMOMWHO_02 BCMOMAGE_02 BCSEX_02 YRBIOCHILD_02 BCAGE_02 BCAGEGRP_02
    ## 1          NA          NA       NA            NA       NA          NA
    ## 2          NA          NA       NA            NA       NA          NA
    ## 3          NA          NA        2          2008       14          NA
    ## 4          NA          NA       NA            NA       NA          NA
    ## 5          NA          NA       NA            NA       NA          NA
    ## 6          NA          NA       NA            NA       NA          NA
    ##   MULTBIRT_02 BCMARLIV_02 BCLRNPRG_02 LIVEHERE_02 ALIVENOW_02 BCNOWLIV_02
    ## 1          NA          NA          NA          NA          NA          NA
    ## 2          NA          NA          NA          NA          NA          NA
    ## 3          NA           1          NA           1          NA          NA
    ## 4          NA          NA          NA          NA          NA          NA
    ## 5          NA          NA          NA          NA          NA          NA
    ## 6          NA          NA          NA          NA          NA          NA
    ##   BCRES_02 BCSIGNBC_02 BCCOURT_02 BCGENTST_02 LIVCHEVR_02 BCWANT_02 BCTIMING_02
    ## 1       NA          NA         NA          NA          NA        NA          NA
    ## 2       NA          NA         NA          NA          NA        NA          NA
    ## 3        0          NA         NA          NA          NA        NA          NA
    ## 4       NA          NA         NA          NA          NA        NA          NA
    ## 5       NA          NA         NA          NA          NA        NA          NA
    ## 6       NA          NA         NA          NA          NA        NA          NA
    ##   BCSOONN_02 BCSOONNMY_02 BCHPY_02 BCMOMWHO_03 BCMOMAGE_03 BCSEX_03
    ## 1         NA           NA       NA          NA          NA       NA
    ## 2         NA           NA       NA          NA          NA       NA
    ## 3         NA           NA       NA          NA          NA        2
    ## 4         NA           NA       NA          NA          NA       NA
    ## 5         NA           NA       NA          NA          NA       NA
    ## 6         NA           NA       NA          NA          NA       NA
    ##   YRBIOCHILD_03 BCAGE_03 BCAGEGRP_03 MULTBIRT_03 BCMARLIV_03 BCLRNPRG_03
    ## 1            NA       NA          NA          NA          NA          NA
    ## 2            NA       NA          NA          NA          NA          NA
    ## 3          2009       12          NA          NA           1          NA
    ## 4            NA       NA          NA          NA          NA          NA
    ## 5            NA       NA          NA          NA          NA          NA
    ## 6            NA       NA          NA          NA          NA          NA
    ##   LIVEHERE_03 ALIVENOW_03 BCNOWLIV_03 BCRES_03 BCSIGNBC_03 BCCOURT_03
    ## 1          NA          NA          NA       NA          NA         NA
    ## 2          NA          NA          NA       NA          NA         NA
    ## 3           1          NA          NA        0          NA         NA
    ## 4          NA          NA          NA       NA          NA         NA
    ## 5          NA          NA          NA       NA          NA         NA
    ## 6          NA          NA          NA       NA          NA         NA
    ##   BCGENTST_03 LIVCHEVR_03 BCWANT_03 BCTIMING_03 BCSOONN_03 BCSOONNMY_03
    ## 1          NA          NA        NA          NA         NA           NA
    ## 2          NA          NA        NA          NA         NA           NA
    ## 3          NA          NA        NA          NA         NA           NA
    ## 4          NA          NA        NA          NA         NA           NA
    ## 5          NA          NA        NA          NA         NA           NA
    ## 6          NA          NA        NA          NA         NA           NA
    ##   BCHPY_03 BCMOMWHO_04 BCMOMAGE_04 BCSEX_04 YRBIOCHILD_04 BCAGE_04 BCAGEGRP_04
    ## 1       NA          NA          NA       NA            NA       NA          NA
    ## 2       NA          NA          NA       NA            NA       NA          NA
    ## 3       NA          NA          NA        2          2011       10          NA
    ## 4       NA          NA          NA       NA            NA       NA          NA
    ## 5       NA          NA          NA       NA            NA       NA          NA
    ## 6       NA          NA          NA       NA            NA       NA          NA
    ##   MULTBIRT_04 BCMARLIV_04 BCLRNPRG_04 LIVEHERE_04 ALIVENOW_04 BCNOWLIV_04
    ## 1          NA          NA          NA          NA          NA          NA
    ## 2          NA          NA          NA          NA          NA          NA
    ## 3          NA           1          NA           1          NA          NA
    ## 4          NA          NA          NA          NA          NA          NA
    ## 5          NA          NA          NA          NA          NA          NA
    ## 6          NA          NA          NA          NA          NA          NA
    ##   BCRES_04 BCSIGNBC_04 BCCOURT_04 BCGENTST_04 LIVCHEVR_04 BCWANT_04 BCTIMING_04
    ## 1       NA          NA         NA          NA          NA        NA          NA
    ## 2       NA          NA         NA          NA          NA        NA          NA
    ## 3        0          NA         NA          NA          NA        NA          NA
    ## 4       NA          NA         NA          NA          NA        NA          NA
    ## 5       NA          NA         NA          NA          NA        NA          NA
    ## 6       NA          NA         NA          NA          NA        NA          NA
    ##   BCSOONN_04 BCSOONNMY_04 BCHPY_04 BCMOMWHO_05 BCMOMAGE_05 BCSEX_05
    ## 1         NA           NA       NA          NA          NA       NA
    ## 2         NA           NA       NA          NA          NA       NA
    ## 3         NA           NA       NA          NA          NA        1
    ## 4         NA           NA       NA          NA          NA       NA
    ## 5         NA           NA       NA          NA          NA       NA
    ## 6         NA           NA       NA          NA          NA       NA
    ##   YRBIOCHILD_05 BCAGE_05 BCAGEGRP_05 MULTBIRT_05 BCMARLIV_05 BCLRNPRG_05
    ## 1            NA       NA          NA          NA          NA          NA
    ## 2            NA       NA          NA          NA          NA          NA
    ## 3          2013        9          NA          NA           1          NA
    ## 4            NA       NA          NA          NA          NA          NA
    ## 5            NA       NA          NA          NA          NA          NA
    ## 6            NA       NA          NA          NA          NA          NA
    ##   LIVEHERE_05 ALIVENOW_05 BCNOWLIV_05 BCRES_05 BCSIGNBC_05 BCCOURT_05
    ## 1          NA          NA          NA       NA          NA         NA
    ## 2          NA          NA          NA       NA          NA         NA
    ## 3           1          NA          NA        0          NA         NA
    ## 4          NA          NA          NA       NA          NA         NA
    ## 5          NA          NA          NA       NA          NA         NA
    ## 6          NA          NA          NA       NA          NA         NA
    ##   BCGENTST_05 LIVCHEVR_05 BCWANT_05 BCTIMING_05 BCSOONN_05 BCSOONNMY_05
    ## 1          NA          NA        NA          NA         NA           NA
    ## 2          NA          NA        NA          NA         NA           NA
    ## 3          NA          NA        NA          NA         NA           NA
    ## 4          NA          NA        NA          NA         NA           NA
    ## 5          NA          NA        NA          NA         NA           NA
    ## 6          NA          NA        NA          NA         NA           NA
    ##   BCHPY_05 BCMOMWHO_06 BCMOMAGE_06 BCSEX_06 YRBIOCHILD_06 BCAGE_06 BCAGEGRP_06
    ## 1       NA          NA          NA       NA            NA       NA          NA
    ## 2       NA          NA          NA       NA            NA       NA          NA
    ## 3       NA          NA          NA        1          2015        6          NA
    ## 4       NA          NA          NA       NA            NA       NA          NA
    ## 5       NA          NA          NA       NA            NA       NA          NA
    ## 6       NA          NA          NA       NA            NA       NA          NA
    ##   MULTBIRT_06 BCMARLIV_06 BCLRNPRG_06 LIVEHERE_06 ALIVENOW_06 BCNOWLIV_06
    ## 1          NA          NA          NA          NA          NA          NA
    ## 2          NA          NA          NA          NA          NA          NA
    ## 3          NA           1          NA           1          NA          NA
    ## 4          NA          NA          NA          NA          NA          NA
    ## 5          NA          NA          NA          NA          NA          NA
    ## 6          NA          NA          NA          NA          NA          NA
    ##   BCRES_06 BCSIGNBC_06 BCCOURT_06 BCGENTST_06 LIVCHEVR_06 BCWANT_06 BCTIMING_06
    ## 1       NA          NA         NA          NA          NA        NA          NA
    ## 2       NA          NA         NA          NA          NA        NA          NA
    ## 3        0          NA         NA          NA          NA        NA          NA
    ## 4       NA          NA         NA          NA          NA        NA          NA
    ## 5       NA          NA         NA          NA          NA        NA          NA
    ## 6       NA          NA         NA          NA          NA        NA          NA
    ##   BCSOONN_06 BCSOONNMY_06 BCHPY_06 BCMOMWHO_07 BCMOMAGE_07 BCSEX_07
    ## 1         NA           NA       NA          NA          NA       NA
    ## 2         NA           NA       NA          NA          NA       NA
    ## 3         NA           NA       NA          NA          NA        2
    ## 4         NA           NA       NA          NA          NA       NA
    ## 5         NA           NA       NA          NA          NA       NA
    ## 6         NA           NA       NA          NA          NA       NA
    ##   YRBIOCHILD_07 BCAGE_07 BCAGEGRP_07 MULTBIRT_07 BCMARLIV_07 BCLRNPRG_07
    ## 1            NA       NA          NA          NA          NA          NA
    ## 2            NA       NA          NA          NA          NA          NA
    ## 3          2017        4          NA          NA           1          NA
    ## 4            NA       NA          NA          NA          NA          NA
    ## 5            NA       NA          NA          NA          NA          NA
    ## 6            NA       NA          NA          NA          NA          NA
    ##   LIVEHERE_07 ALIVENOW_07 BCNOWLIV_07 BCRES_07 BCSIGNBC_07 BCCOURT_07
    ## 1          NA          NA          NA       NA          NA         NA
    ## 2          NA          NA          NA       NA          NA         NA
    ## 3           1          NA          NA        0          NA         NA
    ## 4          NA          NA          NA       NA          NA         NA
    ## 5          NA          NA          NA       NA          NA         NA
    ## 6          NA          NA          NA       NA          NA         NA
    ##   BCGENTST_07 LIVCHEVR_07 BCWANT_07 BCTIMING_07 BCSOONN_07 BCSOONNMY_07
    ## 1          NA          NA        NA          NA         NA           NA
    ## 2          NA          NA        NA          NA         NA           NA
    ## 3          NA          NA         1          NA         NA           NA
    ## 4          NA          NA        NA          NA         NA           NA
    ## 5          NA          NA        NA          NA         NA           NA
    ## 6          NA          NA        NA          NA         NA           NA
    ##   BCHPY_07 BCMOMWHO_08 BCMOMAGE_08 BCSEX_08 YRBIOCHILD_08 BCAGE_08 BCAGEGRP_08
    ## 1       NA          NA          NA       NA            NA       NA          NA
    ## 2       NA          NA          NA       NA            NA       NA          NA
    ## 3       10          NA          NA        1          2019        2          NA
    ## 4       NA          NA          NA       NA            NA       NA          NA
    ## 5       NA          NA          NA       NA            NA       NA          NA
    ## 6       NA          NA          NA       NA            NA       NA          NA
    ##   MULTBIRT_08 BCMARLIV_08 BCLRNPRG_08 LIVEHERE_08 ALIVENOW_08 BCNOWLIV_08
    ## 1          NA          NA          NA          NA          NA          NA
    ## 2          NA          NA          NA          NA          NA          NA
    ## 3          NA           1          NA           1          NA          NA
    ## 4          NA          NA          NA          NA          NA          NA
    ## 5          NA          NA          NA          NA          NA          NA
    ## 6          NA          NA          NA          NA          NA          NA
    ##   BCRES_08 BCSIGNBC_08 BCCOURT_08 BCGENTST_08 LIVCHEVR_08 BCWANT_08 BCTIMING_08
    ## 1       NA          NA         NA          NA          NA        NA          NA
    ## 2       NA          NA         NA          NA          NA        NA          NA
    ## 3        0          NA         NA          NA          NA         2          NA
    ## 4       NA          NA         NA          NA          NA        NA          NA
    ## 5       NA          NA         NA          NA          NA        NA          NA
    ## 6       NA          NA         NA          NA          NA        NA          NA
    ##   BCSOONN_08 BCSOONNMY_08 BCHPY_08 BCMOMWHO_09 BCMOMAGE_09 BCSEX_09
    ## 1         NA           NA       NA          NA          NA       NA
    ## 2         NA           NA       NA          NA          NA       NA
    ## 3         NA           NA       10          NA          NA        2
    ## 4         NA           NA       NA          NA          NA       NA
    ## 5         NA           NA       NA          NA          NA       NA
    ## 6         NA           NA       NA          NA          NA       NA
    ##   YRBIOCHILD_09 BCAGE_09 BCAGEGRP_09 MULTBIRT_09 BCMARLIV_09 BCLRNPRG_09
    ## 1            NA       NA          NA          NA          NA          NA
    ## 2            NA       NA          NA          NA          NA          NA
    ## 3          2022        0          NA          NA           1          NA
    ## 4            NA       NA          NA          NA          NA          NA
    ## 5            NA       NA          NA          NA          NA          NA
    ## 6            NA       NA          NA          NA          NA          NA
    ##   LIVEHERE_09 ALIVENOW_09 BCNOWLIV_09 BCRES_09 BCSIGNBC_09 BCCOURT_09
    ## 1          NA          NA          NA       NA          NA         NA
    ## 2          NA          NA          NA       NA          NA         NA
    ## 3           1          NA          NA        0          NA         NA
    ## 4          NA          NA          NA       NA          NA         NA
    ## 5          NA          NA          NA       NA          NA         NA
    ## 6          NA          NA          NA       NA          NA         NA
    ##   BCGENTST_09 LIVCHEVR_09 BCWANT_09 BCTIMING_09 BCHPY_09 BCSOONN_09
    ## 1          NA          NA        NA          NA       NA         NA
    ## 2          NA          NA        NA          NA       NA         NA
    ## 3          NA          NA         1          NA       10         NA
    ## 4          NA          NA        NA          NA       NA         NA
    ## 5          NA          NA        NA          NA       NA         NA
    ## 6          NA          NA        NA          NA       NA         NA
    ##   BCSOONNMY_09 BCMOMWHO_10 BCMOMAGE_10 BCSEX_10 YRBIOCHILD_10 BCAGE_10
    ## 1           NA          NA          NA       NA            NA       NA
    ## 2           NA          NA          NA       NA            NA       NA
    ## 3           NA          NA          NA        2          2022        0
    ## 4           NA          NA          NA       NA            NA       NA
    ## 5           NA          NA          NA       NA            NA       NA
    ## 6           NA          NA          NA       NA            NA       NA
    ##   BCAGEGRP_10 MULTBIRT_10 BCMARLIV_10 BCLRNPRG_10 LIVEHERE_10 ALIVENOW_10
    ## 1          NA          NA          NA          NA          NA          NA
    ## 2          NA          NA          NA          NA          NA          NA
    ## 3          NA           1          NA          NA          NA          NA
    ## 4          NA          NA          NA          NA          NA          NA
    ## 5          NA          NA          NA          NA          NA          NA
    ## 6          NA          NA          NA          NA          NA          NA
    ##   BCNOWLIV_10 BCRES_10 BCSIGNBC_10 BCCOURT_10 BCGENTST_10 LIVCHEVR_10 BCWANT_10
    ## 1          NA       NA          NA         NA          NA          NA        NA
    ## 2          NA       NA          NA         NA          NA          NA        NA
    ## 3           1        0           1          5           5          NA        NA
    ## 4          NA       NA          NA         NA          NA          NA        NA
    ## 5          NA       NA          NA         NA          NA          NA        NA
    ## 6          NA       NA          NA         NA          NA          NA        NA
    ##   BCTIMING_10 BCSOONN_10 BCSOONNMY_10 BCHPY_10 CWPKIDS NBPARENT NBKDLEGSTAT
    ## 1          NA         NA           NA       NA       0       NA          NA
    ## 2          NA         NA           NA       NA       0       NA          NA
    ## 3          NA         NA           NA       NA       1       NA          NA
    ## 4          NA         NA           NA       NA       1       NA          NA
    ## 5          NA         NA           NA       NA       0       NA          NA
    ## 6          NA         NA           NA       NA       0       NA          NA
    ##   NBKADOP1 NBKADOP2 NBKGUARD EVERADOPT OTPREG OTPRGPRB OTPRGN OTPREGS PREGSNOW
    ## 1       NA       NA       NA        NA     NA       NA     NA       0        0
    ## 2       NA       NA       NA         5      5        5     NA       0        0
    ## 3       NA       NA       NA         5      1       NA      1       1        0
    ## 4       NA       NA       NA         5      5        5     NA       0        0
    ## 5       NA       NA       NA        NA      5        5     NA       0        0
    ## 6       NA       NA       NA        NA      5        5     NA       0        0
    ##   PREGCHK TOTPREGS_R TOTPREGS_CON ANYKIDS CRALL CRALLU5 CRALL518 CRMALU5
    ## 1      NA         NA           NA       5    NA      NA       NA      NA
    ## 2       1         NA            0       5     0       0        0       0
    ## 3       1         NA           10       1     4       2        3       1
    ## 4       1         NA            1       1     1       0        1       0
    ## 5       1         NA            0       5     0       0        0       0
    ## 6       1         NA            0       5     0       0        0       0
    ##   CRMAL518 CRFEMU5 CRFEM518 NCALL NCALLU5 NCALL518 NCMALU5 NCMAL518 NCFEMU5
    ## 1       NA      NA       NA    NA      NA       NA      NA       NA      NA
    ## 2        0       0        0     0       0        0       0        0       0
    ## 3        2       2        2     0       0        0       0        0       0
    ## 4        1       0        0     0       0        0       0        0       0
    ## 5        0       0        0     0       0        0       0        0       0
    ## 6        0       0        0     0       0        0       0        0       0
    ##   NCFEM518 RFAGE RFSEX ROUTG04 RMEAL04 RERRAND04 RPLAY04 RREAD04 RAFFECT04
    ## 1       NA    NA    NA      NA      NA        NA      NA      NA        NA
    ## 2        0    NA    NA      NA      NA        NA      NA      NA        NA
    ## 3        0     0     2       2       5         1       4       1         4
    ## 4        0     7     1      NA      NA        NA      NA      NA        NA
    ## 5        0    NA    NA      NA      NA        NA      NA      NA        NA
    ## 6        0    NA    NA      NA      NA        NA      NA      NA        NA
    ##   RPRAISE04 RFEED04 RBATH04 RDIAPER04 RBED04 RAPPT04 RDISC04 ROUTG518 RMEAL518
    ## 1        NA      NA      NA        NA     NA      NA      NA       NA       NA
    ## 2        NA      NA      NA        NA     NA      NA      NA       NA       NA
    ## 3         1       1       1         1      4       2       1       NA       NA
    ## 4        NA      NA      NA        NA     NA      NA      NA        4        4
    ## 5        NA      NA      NA        NA     NA      NA      NA       NA       NA
    ## 6        NA      NA      NA        NA     NA      NA      NA       NA       NA
    ##   RERRAND518 RAFFECT518 RPRAISE518 RTAKE518 RAPPT518 RHELP518 RDISC518 RCLFR518
    ## 1         NA         NA         NA       NA       NA       NA       NA       NA
    ## 2         NA         NA         NA       NA       NA       NA       NA       NA
    ## 3         NA         NA         NA       NA       NA       NA       NA       NA
    ## 4          2          5          5        3        1        3        4        2
    ## 5         NA         NA         NA       NA       NA       NA       NA       NA
    ## 6         NA         NA         NA       NA       NA       NA       NA       NA
    ##   RDO518 NRFAGE NRFSEX NRVISIT04 NRSATVIS04 NROUTG04 NRMEAL04 NRERRAND04
    ## 1     NA     NA     NA        NA         NA       NA       NA         NA
    ## 2     NA     NA     NA        NA         NA       NA       NA         NA
    ## 3     NA     NA     NA        NA         NA       NA       NA         NA
    ## 4      1     NA     NA        NA         NA       NA       NA         NA
    ## 5     NA     NA     NA        NA         NA       NA       NA         NA
    ## 6     NA     NA     NA        NA         NA       NA       NA         NA
    ##   NROVRNT04 NRPLAY04 NRREAD04 NRAFFECT04 NRPRAISE04 NRFEED04 NRBATH04
    ## 1        NA       NA       NA         NA         NA       NA       NA
    ## 2        NA       NA       NA         NA         NA       NA       NA
    ## 3        NA       NA       NA         NA         NA       NA       NA
    ## 4        NA       NA       NA         NA         NA       NA       NA
    ## 5        NA       NA       NA         NA         NA       NA       NA
    ## 6        NA       NA       NA         NA         NA       NA       NA
    ##   NRDIAPER04 NRBED04 NRAPPT04 NRDISC04 NRVISIT518 NRSATVIS518 NROUTG518
    ## 1         NA      NA       NA       NA         NA          NA        NA
    ## 2         NA      NA       NA       NA         NA          NA        NA
    ## 3         NA      NA       NA       NA         NA          NA        NA
    ## 4         NA      NA       NA       NA         NA          NA        NA
    ## 5         NA      NA       NA       NA         NA          NA        NA
    ## 6         NA      NA       NA       NA         NA          NA        NA
    ##   NRMEAL518 NRERRAND518 NROVRNT518 NRAFFECT518 NRPRAISE518 NRTAKE518 NRAPPT518
    ## 1        NA          NA         NA          NA          NA        NA        NA
    ## 2        NA          NA         NA          NA          NA        NA        NA
    ## 3        NA          NA         NA          NA          NA        NA        NA
    ## 4        NA          NA         NA          NA          NA        NA        NA
    ## 5        NA          NA         NA          NA          NA        NA        NA
    ## 6        NA          NA         NA          NA          NA        NA        NA
    ##   NRHELP518 NRDISC518 NRCLFR518 NRDO518 COPARENT RWANT PROBWANT JINTEND
    ## 1        NA        NA        NA      NA       NA     5       NA      NA
    ## 2        NA        NA        NA      NA       NA     1       NA       1
    ## 3        NA        NA        NA      NA       NA     1       NA       9
    ## 4        NA        NA        NA      NA       NA     5       NA       5
    ## 5        NA        NA        NA      NA       NA     1       NA      NA
    ## 6        NA        NA        NA      NA       NA     1       NA      NA
    ##   JSUREINT JINTENDN JEXPECTL JEXPECTS JINTNEXT INTEND INTENDN EXPECTL EXPECTS
    ## 1       NA       NA       NA       NA       NA     NA      NA      NA      NA
    ## 2        1        2       NA       NA        3     NA      NA      NA      NA
    ## 3       NA       NA        2        0        1     NA      NA      NA      NA
    ## 4        1       NA       NA       NA       NA     NA      NA      NA      NA
    ## 5       NA       NA       NA       NA       NA      1       3      NA      NA
    ## 6       NA       NA       NA       NA       NA      1       2      NA      NA
    ##   INTNEXT USUALCAR USLPLACE USL12MOS CURRCOV COVERHOW_01 COVERHOW_02
    ## 1      NA        5       NA       NA       5          NA          NA
    ## 2      NA        1        1        1       1           1          NA
    ## 3      NA        1        1        1       5          NA          NA
    ## 4      NA        1        1        1       1           1           6
    ## 5       3        1        9        5       1          99          NA
    ## 6       3        1        9        5       1           2           9
    ##   COVERHOW_03 PARINSUR COVER12 NUMNOCOV YOUGOFPC WHENGOFP YOUFPSVC_1 YOUFPSVC_2
    ## 1          NA       NA       1       12        5       NA         NA         NA
    ## 2          NA       NA       5       NA        5       NA         NA         NA
    ## 3          NA       NA       1       12        5       NA         NA         NA
    ## 4          NA       NA       5       NA        5       NA         NA         NA
    ## 5          NA       NA       5       NA        5       NA         NA         NA
    ## 6          NA       NA       5       NA        5       NA         NA         NA
    ##   YOUFPSVC_3 YOUFPSVC_4 YOUFPSVC_5 YOUFPSVC_6 YOUFPSVC_7 VISION HEARING
    ## 1         NA         NA         NA         NA         NA      1       1
    ## 2         NA         NA         NA         NA         NA      1       1
    ## 3         NA         NA         NA         NA         NA      1       1
    ## 4         NA         NA         NA         NA         NA      1       1
    ## 5         NA         NA         NA         NA         NA      2       1
    ## 6         NA         NA         NA         NA         NA      1       1
    ##   MOBILITY COGNITION SELFCARE COMMUNIC EVRCANCER AGECANCER ALCORISK VISIT12MO
    ## 1        1         1        1        1         5        NA        4         5
    ## 2        1         1        1        1         5        NA        2         1
    ## 3        1         1        1        1         5        NA        4         1
    ## 4        1         1        1        1         5        NA        2         1
    ## 5        1         1        1        1         5        NA        2         1
    ## 6        1         2        1        1         5        NA        1         1
    ##   SVC12MO_1 SVC12MO_2 SVC12MO_3 SVC12MO_4 SVC12MO_5 SVC12MO_6 SVC12MO_7
    ## 1        NA        NA        NA        NA        NA        NA        NA
    ## 2        10        NA        NA        NA        NA        NA        NA
    ## 3         1        NA        NA        NA        NA        NA        NA
    ## 4        10        NA        NA        NA        NA        NA        NA
    ## 5        10        NA        NA        NA        NA        NA        NA
    ## 6        10        NA        NA        NA        NA        NA        NA
    ##   SVC12MO_8 SVC12MO_9 NUMVISIT PLACEVIS_01 PLACEVIS_02 PLACEVIS_03 PLACEVIS_04
    ## 1        NA        NA       NA          NA          NA          NA          NA
    ## 2        NA        NA        4           1          NA          NA          NA
    ## 3        NA        NA        1           1          NA          NA          NA
    ## 4        NA        NA        1           1          NA          NA          NA
    ## 5        NA        NA        1           1          NA          NA          NA
    ## 6        NA        NA        2           7           9          NA          NA
    ##   PLACEVIS_05 PLACEVIS_06 SVCPAY_1 SVCPAY_2 SVCPAY_3 SVCPAY_4 TALKSA TALKEC
    ## 1          NA          NA       NA       NA       NA       NA     NA     NA
    ## 2          NA          NA        5       NA       NA       NA      1      5
    ## 3          NA          NA        3       NA       NA       NA      5      5
    ## 4          NA          NA        1       NA       NA       NA      5      5
    ## 5          NA          NA       99       NA       NA       NA      1      5
    ## 6          NA          NA        4       NA       NA       NA      1      5
    ##   TALKDM WHYPSTD WHYNOSTD BARRIER_01 BARRIER_02 BARRIER_03 BARRIER_04
    ## 1     NA      NA       NA          1         NA         NA         NA
    ## 2      5      NA        7         NA         NA         NA         NA
    ## 3      5      NA        3         NA         NA         NA         NA
    ## 4      5      NA        3         NA         NA         NA         NA
    ## 5      9      NA        9         NA         NA         NA         NA
    ## 6      5      NA        7         NA         NA         NA         NA
    ##   BARRIER_05 BARRIER_06 BARRIER_07 BARRIER_08 EVERVACC HPVSHOT1 BLDPRESS HIGHBP
    ## 1         NA         NA         NA         NA        5       NA        5     NA
    ## 2         NA         NA         NA         NA        5       NA        1      5
    ## 3         NA         NA         NA         NA        5       NA        1      5
    ## 4         NA         NA         NA         NA        5       NA        1      5
    ## 5         NA         NA         NA         NA        5       NA        5     NA
    ## 6         NA         NA         NA         NA        5       NA        1      5
    ##   BPMEDS BPMON BPMONFRQ ASKSMOKE INFHELP INFSVCS_1 INFSVCS_2 INFSVCS_3
    ## 1     NA    NA       NA        5       7        NA        NA        NA
    ## 2     NA    NA       NA        1       5        NA        NA        NA
    ## 3     NA    NA       NA        1       5        NA        NA        NA
    ## 4     NA    NA       NA        1       5        NA        NA        NA
    ## 5     NA    NA       NA        1       5        NA        NA        NA
    ## 6     NA    NA       NA        1       5        NA        NA        NA
    ##   INFSVCS_4 INFSVCS_5 INFSVCS_6 INFHLPNW LASTHELP INFRTHIS_1 INFRTHIS_2
    ## 1        NA        NA        NA       NA       NA         NA         NA
    ## 2        NA        NA        NA       NA       NA         NA         NA
    ## 3        NA        NA        NA       NA       NA         NA         NA
    ## 4        NA        NA        NA       NA       NA         NA         NA
    ## 5        NA        NA        NA       NA       NA         NA         NA
    ## 6        NA        NA        NA       NA       NA         NA         NA
    ##   INFRTHIS_3 DONBLOOD DONBLDYR HIVTEST WHNHIVTST PLCHIV RHHIVT1 RHHIVT2_1
    ## 1         NA        5       NA       5        NA     NA      NA        NA
    ## 2         NA        5       NA       1         4      1      NA        NA
    ## 3         NA        1        5       9        NA     NA      NA        NA
    ## 4         NA        1        5       5        NA     NA      NA        NA
    ## 5         NA        5       NA       5        NA     NA      NA        NA
    ## 6         NA        5       NA       9        NA     NA      NA        NA
    ##   RHHIVT2_2 HIVTST PREPHIV PREP12 TALKDOCT AIDSTALK_01 AIDSTALK_02 AIDSTALK_03
    ## 1        NA     NA       5     NA        5          NA          NA          NA
    ## 2        NA      9       5     NA        5          NA          NA          NA
    ## 3        NA     NA       5     NA        5          NA          NA          NA
    ## 4        NA     NA       1      5        5          NA          NA          NA
    ## 5        NA     NA       5     NA        1           1           2           5
    ## 6        NA     NA       5     NA        5          NA          NA          NA
    ##   AIDSTALK_04 AIDSTALK_05 AIDSTALK_06 AIDSTALK_07 AIDSTALK_08 AIDSTALK_09
    ## 1          NA          NA          NA          NA          NA          NA
    ## 2          NA          NA          NA          NA          NA          NA
    ## 3          NA          NA          NA          NA          NA          NA
    ## 4          NA          NA          NA          NA          NA          NA
    ## 5           9          NA          NA          NA          NA          NA
    ## 6          NA          NA          NA          NA          NA          NA
    ##   AIDSTALK_10 AIDSTALK_11 AIDSTALK_12 SAMEADD BRNOUT ATTND14 FUNDAM_1 FUNDAM_2
    ## 1          NA          NA          NA       1      5      NA       NA       NA
    ## 2          NA          NA          NA       5      1      NA        5       NA
    ## 3          NA          NA          NA       1      5      NA        1       NA
    ## 4          NA          NA          NA       1      5      NA        5       NA
    ## 5          NA          NA          NA       1      5       6        5       NA
    ## 6          NA          NA          NA       1      5       2        1       NA
    ##   FUNDAM_3 FUNDAM_4 RELDLIFE ATTNDNOW MILSVC WRK12MOS FPT12MOS DOLASTWK1
    ## 1       NA       NA       NA        7      2        1        1         1
    ## 2       NA       NA        1        2      2        1        1         1
    ## 3       NA       NA        1        1      2        1        1         1
    ## 4       NA       NA        3        6      2        1        1         1
    ## 5       NA       NA        3        5     NA        5       NA         4
    ## 6       NA       NA        2        2     NA        5       NA         4
    ##   DOLASTWK2 DOLASTWK3 DOLASTWK4 DOLASTWK5 DOLASTWK6 RWRKST RFTPTX SPLSTWK1
    ## 1        NA        NA        NA        NA        NA      1      2       NA
    ## 2        NA        NA        NA        NA        NA      1      2        1
    ## 3         5        NA        NA        NA        NA      1      2        5
    ## 4        NA        NA        NA        NA        NA      1      2        1
    ## 5        NA        NA        NA        NA        NA      5     NA       NA
    ## 6         3        NA        NA        NA        NA      5     NA       NA
    ##   SPLSTWK2 SPLSTWK3 SPLSTWK4 SPLSTWK5 SPLSTWK6 SPWRKST SPFTPTX REACTSLF
    ## 1       NA       NA       NA       NA       NA      NA      NA        1
    ## 2       NA       NA       NA       NA       NA       1       2        4
    ## 3       NA       NA       NA       NA       NA       5      NA        4
    ## 4       NA       NA       NA       NA       NA       1       2        1
    ## 5       NA       NA       NA       NA       NA      NA      NA        5
    ## 6       NA       NA       NA       NA       NA      NA      NA        2
    ##   CHBOTHER SEXNEEDS WHENSICK SHOWPAIN CASILANG GENHEALT BMIcat DRWEIGH TELLWGHT
    ## 1        4        3        3        4        1        2      4       5       NA
    ## 2        9        5        5        4        2        1      3       1        5
    ## 3        4        2        3        3        1        2      5       1        2
    ## 4        4        2        4        4        1        1      2       1        5
    ## 5        2        1        3        2        1        1     NA       1        2
    ## 6        1        3        3        2        1        3     NA       1        3
    ##   WGHTSCRN ENGSPEAK NOBEDYR STAYREL JAILED JAILED2 FRQJAIL FRQJAIL2 EVSUSPEN
    ## 1       NA        1       5       5      5       5      NA       NA       NA
    ## 2        5        2       1       5      5       5      NA       NA       NA
    ## 3       NA        2       5       5      5       5      NA       NA       NA
    ## 4        5        1       5       5      5       5      NA       NA       NA
    ## 5       NA        1       5       5      5       5      NA       NA        5
    ## 6        5        1       5       5      5       5      NA       NA        5
    ##   GRADSUSP SMK100 AGESMK SMOKE30 DRINK12 BINGE12 POT12 FEMTOUCH VAGSEX AGEVAGR
    ## 1       NA      1     95       1       2       1     6       NA     NA      NA
    ## 2       NA      1     15       1       3       3     1       NA     NA      NA
    ## 3       NA      5     NA      NA       3       1     1       NA     NA      NA
    ## 4       NA      5     NA      NA       5       5     1       NA     NA      NA
    ## 5       NA      5     NA      NA       4       4     4        1      1      16
    ## 6       NA      5     NA      NA       2       1     4        1      1      14
    ##   CONDVAG COND1BRK COND1OFF WHYCONDL GETORALF CONDFELL GIVORALF ANYORAL
    ## 1      NA       NA       NA       NA        5       NA        5       5
    ## 2       1        5        5        1        1        5        1       1
    ## 3       5       NA       NA       NA        1        5        1       1
    ## 4       1        5        5        1        1        5        1       1
    ## 5       5       NA       NA       NA        1        5        1       1
    ## 6       1        5        5        3        5       NA        5       5
    ##   K_HADSEX TIMING ANALSEX CONDANAL OPPSEXANY OPPSEXGEN CONDSEXL OPPLIFENUM
    ## 1        5     NA       5       NA         5         5       NA         NA
    ## 2        1     NA       1        1         1         1        1         15
    ## 3        1     NA       5       NA         1         1       NA          1
    ## 4        1     NA       1        1         1         1        1          3
    ## 5        1      5       1        5         1         1       NA          4
    ## 6        1     NA       5       NA         1         1        1          1
    ##   OPPYEARNUM VAGNUM12 ORALNUM12 ANALNUM12 RNONMONOG NONMONOG NNONMONOG FEMSHT12
    ## 1         NA       NA        NA        NA        NA       NA        NA       NA
    ## 2          1        1         1         1        NA        5        NA        5
    ## 3          1        1         1        NA        NA        5        NA        5
    ## 4          1        1         1         0        NA        5        NA        5
    ## 5          2        4         4         0         5        5        NA        5
    ## 6          1        1        NA        NA        NA        5        NA        5
    ##   JOHNFREQ PROSTFRQ GIVORALM GETORALM ORALCONDM ANALSEX2 ANALCONDM1 ANALSEX3
    ## 1       NA       NA        5        5        NA        5         NA        5
    ## 2        5        5       NA       NA        NA       NA         NA       NA
    ## 3        5        5        5        5        NA        5         NA        5
    ## 4        5        5        5        5        NA        5         NA        5
    ## 5        5        5        5        5        NA        5         NA        5
    ## 6        5        5        5        5        NA        5         NA        5
    ##   ANALCONDM2 MALESEX SAMESEXANY MALPRTAGE SAMLIFENUM SAMYEARNUM SAMORAL12
    ## 1         NA       5          5        NA         NA         NA        NA
    ## 2         NA      NA         NA        NA         NA         NA        NA
    ## 3         NA       5          5        NA         NA         NA        NA
    ## 4         NA       5          5        NA         NA         NA        NA
    ## 5         NA       5          5        NA         NA         NA        NA
    ## 6         NA       5          5        NA         NA         NA        NA
    ##   RECEPANAL12 INSERANAL12 SAMESEX1 MSAMEREL MALEGSTAT MALMARRN MALCOHN
    ## 1          NA          NA       NA       NA        NA       NA      NA
    ## 2          NA          NA       NA       NA        NA       NA      NA
    ## 3          NA          NA       NA       NA        NA       NA      NA
    ## 4          NA          NA       NA       NA        NA       NA      NA
    ## 5          NA          NA       NA       NA        NA       NA      NA
    ## 6          NA          NA       NA       NA        NA       NA      NA
    ##   MSMNONMON MALSHT12 JOHN2FRQ PROS2FRQ MSMSORT12 CNDLSMAL CONDALLS MFLASTP
    ## 1        NA       NA       NA       NA        NA       NA       NA      NA
    ## 2        NA       NA       NA       NA        NA       NA       NA      NA
    ## 3        NA       NA       NA       NA        NA       NA       NA      NA
    ## 4        NA       NA       NA       NA        NA       NA       NA      NA
    ## 5        NA       NA       NA       NA        NA       NA       NA      NA
    ## 6        NA       NA       NA       NA        NA       NA       NA      NA
    ##   WHYCOND DATEAPP ATTRACT ORIENT CONFCONC TIMALON RISKCHEK1 RISKCHEK2 RISKCHEK3
    ## 1      NA       5       1      2       NA      NA         5         5         5
    ## 2      NA      NA      NA     NA       NA      NA        NA        NA        NA
    ## 3      NA       5       8      2       NA      NA         5         5         5
    ## 4      NA       5       1      2       NA      NA         5         5         5
    ## 5      NA      NA       1      2        5       6         1         5         5
    ## 6      NA      NA       1      2        5       5         1         1         1
    ##   RISKCHEK4 RECTDOUCH STDTST12 STDSITE12 STDTRT12 GON CHLAM HERPES GENWARTS
    ## 1         5        NA        5        NA        5   5     5      5        5
    ## 2        NA        NA       NA        NA       NA  NA    NA     NA       NA
    ## 3         5        NA        5        NA        5   5     5      5        5
    ## 4         5        NA        5        NA        5   5     5      5        5
    ## 5         5        NA        5        NA        5   5     5      5        5
    ## 6         1        NA        5        NA        5   5     5      5        5
    ##   SYPHILIS EMOTABUSE PHYSABUSE SEXABUSE REVPHYSNEG REVEMOTNEG WITNESSIPV
    ## 1        5         3         2        1          5          5          1
    ## 2       NA        NA        NA       NA         NA         NA         NA
    ## 3        5         2         1        1          5          5          1
    ## 4        5         2         1        1          5          5          1
    ## 5        5         2         1       NA          5          5          1
    ## 6        5         3         1       NA          1          5          1
    ##   LIVDRUGS LIVDEPRESS SEPJAIL RACEDESCRIM GENDDESCRIM WITVIOL EARNTYPE EARN
    ## 1        5          5       5           1           1       1        3    8
    ## 2       NA         NA      NA          NA          NA      NA       NA   NA
    ## 3        5          1       5           1           1       1        2   15
    ## 4        5          5       5           1           1       1        3   14
    ## 5        5          5       5           1           1       1       NA   NA
    ## 6        5          5       1           1           2       1       NA   NA
    ##   EARNDK1 EARNDK2 EARNDK3 EARNDK4 TOINCWMY TOTINC FMINCDK1 FMINCDK2 FMINCDK3
    ## 1      NA      NA      NA      NA        3     13       NA       NA       NA
    ## 2      NA      NA      NA      NA       NA     NA       NA       NA       NA
    ## 3      NA      NA      NA      NA        3     15       NA       NA       NA
    ## 4      NA      NA      NA      NA        3     15       NA       NA       NA
    ## 5      NA      NA      NA      NA        3     15       NA       NA       NA
    ## 6      NA      NA      NA      NA        1      5       NA       NA       NA
    ##   FMINCDK4 FMINCDK5 PUBASST FOODSTMP WIC HLPTRANS HLPCHLDC HLPJOB FREEFOOD
    ## 1       NA       NA       5        5   5        5        5      5        5
    ## 2       NA       NA      NA       NA  NA       NA       NA     NA       NA
    ## 3       NA       NA       5        5   5        5        5      5        5
    ## 4       NA       NA       5        5   5        5        5      5        5
    ## 5       NA       NA       5        5   5        5        5      5        5
    ## 6       NA       NA       1        1   5        5        5      5        5
    ##   HUNGRY MED_COST COVIDVAX COVVAX_M COVVAX_Y CMCOVVAX HADCOVID AGER FMARITAL
    ## 1      5        5        1        9     2021     1461        5   27        5
    ## 2     NA       NA       NA       NA       NA       NA       NA   31        1
    ## 3      5        5        5       NA       NA       NA        5   37        1
    ## 4      5        5        1        1     2021     1453        1   40        1
    ## 5      5        5        5       NA       NA       NA        5   17        5
    ## 6      5        5        5       NA       NA       NA        5   15        5
    ##   RMARITAL HIEDUC HIEDUC_I HISPANIC HISPANIC_I HISPRACE2 HISPRACE2_I NUMKDHH
    ## 1        6      4        0        1          0         1           0       0
    ## 2        1      6        0        1          0         1           0       0
    ## 3        1      1        0        2          0         2           0       4
    ## 4        1      9        0        2          0         2           0       1
    ## 5        6      2        0        1          0         1           0       0
    ## 6        6      1        0        2          0         2           0       0
    ##   NUMFMHH HHFAMTYP HHFAMTYP_I HHPARTYP NCHILDHH HHKIDTYP CSPBBHH CSPSBHH
    ## 1       2        1          0        1        0        0      NA      NA
    ## 2       1        1          0        4        0        0       0       0
    ## 3       6        3          0        4        3        1       3       0
    ## 4       2        3          0        4        1        1       1       0
    ## 5       3        1          0        1        0        0      NA      NA
    ## 6       2        1          0        3        0        0      NA      NA
    ##   CSPOKDHH INTCTFAM INTCTFAM_I PARAGE14 PARAGE14_I EDUCMOM EDUCMOM_I AGEMOMB1
    ## 1       NA        1          0        1          0       1         0        3
    ## 2        0        1          0        1          0       4         0        3
    ## 3        0        1          0        1          0       1         0        3
    ## 4        0        1          0        1          0       2         0        4
    ## 5       NA        1          0        1          0       2         0        3
    ## 6       NA        2          0        3          0       3         0        3
    ##   AGEMOMB1_I HADSEX LSEXDATE LSEXDATE_I lsexrage sex3mo sex12mo LSEXRLTN
    ## 1          0      2       NA          0       NA     NA      NA       NA
    ## 2          0      1     1478          0       31      1       1        1
    ## 3          0      1     1474          0       37      1       1        1
    ## 4          0      1     1484          0       40      1       1        1
    ## 5          0      1     1473          0       17      1       1        7
    ## 6          0      1     1451          0       13      2       2        5
    ##   LSEXRLTN_I LSEXUSE1 LSEXUSE1_I LSEXUSE2 LSEXUSE2_I LSEXUSE3 LSEXUSE3_I
    ## 1          0       NA          0       NA          0       NA          0
    ## 2          0        1          0       NA          0       NA          0
    ## 3          0       96          0       96          0       96          0
    ## 4          0        1          0        4          0       NA          0
    ## 5          0       96          0       96          0       96          0
    ## 6          0        1          0       NA          0       NA          0
    ##   LSEXUSE4 LSEXUSE4_I meth12m1 meth12m2 meth12m3 meth12m4 meth3m1 meth3m2
    ## 1       NA          0       NA       NA       NA       NA      NA      NA
    ## 2       NA          0        1       NA       NA       NA       1      NA
    ## 3       96          0       96       96       96       96      96      96
    ## 4       NA          0        1        4       NA       NA       1       4
    ## 5       96          0       96       96       96       96      96      96
    ## 6       NA          0       NA       NA       NA       NA      NA      NA
    ##   meth3m3 meth3m4 PARTS1YR PARTS1YR_I PARTDUR1 PARTDUR2 PARTDUR3 PARTDUR1_I
    ## 1      NA      NA        0          0       NA       NA       NA          0
    ## 2      NA      NA        1          0       49       NA       NA          0
    ## 3      96      96        1          0      204       NA       NA          0
    ## 4      NA      NA        1          0      239       NA       NA          0
    ## 5      96      96        2          0      997        0       NA          0
    ## 6      NA      NA        0          0      997       NA       NA          0
    ##   PARTDUR2_I PARTDUR3_I NUMP3MOS NUMP3MOS_I LIFPRTNR LIFPRTNR_I FMARNO COHEVER
    ## 1          0          0       NA          0        0          0      0       2
    ## 2          0          0        1          0       15          0      2       1
    ## 3          0          0        1          0        1          0      1       2
    ## 4          0          0        1          0        3          0      1       2
    ## 5          0          0        1          0        4          0      0       2
    ## 6          0          0        0          0        1          0      0       2
    ##   COHEVER_I evmarcoh SEXONCE SEXONCE_I VRY1STSX VRY1STSX_I vry1stag FIRSTPFLAG
    ## 1         0        2      NA         0       NA          0       NA         NA
    ## 2         0        1       2         0     1290          0       15          1
    ## 3         0        1       2         0     1270          0       20          8
    ## 4         0        1       2         0     1209          0       17          1
    ## 5         0        2       2         0     1442          0       14          1
    ## 6         0        2       1         0     1451          0       13          2
    ##   FSEXRLTN FSEXRLTN_I SEX1MTHD1 SEX1MTHD1_I SEX1MTHD2 SEX1MTHD2_I SEX1MTHD3
    ## 1       NA          0        NA           0        NA           0        NA
    ## 2        7          0         1           0        NA           0        NA
    ## 3        1          0        96           0        96           0        96
    ## 4        5          0         1           0         4           0        NA
    ## 5        5          0        96           0        96           0        96
    ## 6        6          0         1           0        NA           0        NA
    ##   SEX1MTHD3_I SEX1MTHD4 SEX1MTHD4_I MARDAT01 MARDAT01_I FMAR1AGE MAREND01
    ## 1           0        NA           0       NA          0       NA       NA
    ## 2           0        NA           0     2018          0       26        2
    ## 3           0        96           0     2005          0       20       NA
    ## 4           0        NA           0     2010          0       26       NA
    ## 5           0        96           0       NA          0       NA       NA
    ## 6           0        NA           0       NA          0       NA       NA
    ##   MAREND01_I MARDIS01 MARDIS01_I PREMARW1 mar1diss COHAB1 COHAB1_I COHSTAT
    ## 1          0       NA          0       NA       NA     NA        0       1
    ## 2          0     2018          0        2        1   2021        0       3
    ## 3          0       NA          0        2        5     NA        0       1
    ## 4          0       NA          0        2        5     NA        0       1
    ## 5          0       NA          0       NA       NA     NA        0       1
    ## 6          0       NA          0       NA       NA     NA        0       1
    ##   COHSTAT_I COHOUT COH1DUR COH1DUR_I sexmar sexunion CSPBIOKD CSPBIOKD_I
    ## 1         0     NA      NA         0     NA       NA       NA          0
    ## 2         0     NA      NA         0      4        4        0          0
    ## 3         0     NA      NA         0      1        1       10          0
    ## 4         0     NA      NA         0      4        4        1          0
    ## 5         0     NA      NA         0      3        3       NA          0
    ## 6         0     NA      NA         0      3        3       NA          0
    ##   DATBABY1 DATBABY1_I agebaby1 b1premar MARBABY1 MARBABY1_I COMPREG COMPREG_I
    ## 1       NA          0       NA       NA       NA          0       0         0
    ## 2       NA          0       NA       NA       NA          0       0         0
    ## 3     2006          0       21        2        1          0      10         0
    ## 4     2016          0       33        2        1          0       1         0
    ## 5       NA          0       NA       NA       NA          0       0         0
    ## 6       NA          0       NA       NA       NA          0       0         0
    ##   WANTB1 WANTB1_I DADTYPE DADTYPE_I INTENT ADDEXP ADDEXP_I CURR_INS CURR_INS_I
    ## 1     NA        0       4         0      2      0        0        4          0
    ## 2     NA        0       4         0      1     20        0        1          0
    ## 3     NA        0       1         0      3     10        0        4          0
    ## 4     NA        0       1         0      2      0        0        1          0
    ## 5     NA        0       4         0      1     30        0        1          1
    ## 6     NA        0       4         0      1     20        0        2          0
    ##   EVHIVTST RELIGION RELIGION_I LABORFOR LABORFOR_I TOTINCR TOTINCR_I POVERTY
    ## 1        0        1          0        1          0      13         0     313
    ## 2        2        2          0        1          0      15         1     635
    ## 3       NA        3          0        1          0      15         0     222
    ## 4        1        2          0        1          0      15         0     537
    ## 5        0        2          0        5          0      15         0     451
    ## 6       NA        3          0        4          0       5         0      59
    ##   POVERTY_I METRO WGT2022_2023 VEST VECL CMINTVW CMLSTYR CMFIVYR YEAR QUARTER
    ## 1         0     1     7509.369   17    1    1468    1456    1408    1       2
    ## 2         1     1     4626.890    8    1    1478    1466    1418    2       1
    ## 3         0     3    46933.862   10    2    1474    1462    1414    1       4
    ## 4         0     3    16872.662   10    1    1484    1472    1424    2       3
    ## 5         0     2    30201.388   15    1    1474    1462    1414    1       3
    ## 6         0     3    14732.608   17    2    1479    1467    1419    2       1
    ##   PHASE1 PHASE2 PHASE3
    ## 1      1      0      0
    ## 2      1      1      0
    ## 3      1      1      0
    ## 4      1      1      0
    ## 5      1      1      1
    ## 6      1      1      0

``` r
#data cleaning

#checking of missing values
summary(maleresp)
```

    ##      CaseID          RSCRAGE        RSCRNINF        RSCRHISP    
    ##  Min.   : 96063   Min.   :15.0   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.: 98511   1st Qu.:24.0   1st Qu.:1.000   1st Qu.:5.000  
    ##  Median :101048   Median :32.0   Median :1.000   Median :5.000  
    ##  Mean   :101025   Mean   :31.7   Mean   :2.985   Mean   :4.252  
    ##  3rd Qu.:103495   3rd Qu.:39.0   3rd Qu.:5.000   3rd Qu.:5.000  
    ##  Max.   :106018   Max.   :49.0   Max.   :5.000   Max.   :5.000  
    ##                                                  NA's   :1      
    ##     RSCRRACE        FTFMODE     DEVICE_TYPE            AGE_R      
    ##  Min.   :1.000   Min.   :1.00   Length:4371        Min.   :15.00  
    ##  1st Qu.:2.000   1st Qu.:1.00   Class :character   1st Qu.:24.00  
    ##  Median :3.000   Median :2.00   Mode  :character   Median :32.00  
    ##  Mean   :2.824   Mean   :1.73                      Mean   :31.78  
    ##  3rd Qu.:3.000   3rd Qu.:2.00                      3rd Qu.:40.00  
    ##  Max.   :4.000   Max.   :2.00                      Max.   :50.00  
    ##                                                                   
    ##     AGESCRN           HISP          HISPGRP          ROSCNT        HHKIDS18    
    ##  Min.   :15.00   Min.   :1.000   Min.   :1.000   Min.   :1.00   Min.   :0.000  
    ##  1st Qu.:24.00   1st Qu.:5.000   1st Qu.:1.000   1st Qu.:2.00   1st Qu.:0.000  
    ##  Median :32.00   Median :5.000   Median :1.000   Median :3.00   Median :0.000  
    ##  Mean   :31.76   Mean   :4.209   Mean   :1.648   Mean   :2.92   Mean   :0.517  
    ##  3rd Qu.:39.00   3rd Qu.:5.000   3rd Qu.:2.000   3rd Qu.:4.00   3rd Qu.:1.000  
    ##  Max.   :49.00   Max.   :9.000   Max.   :9.000   Max.   :8.00   Max.   :4.000  
    ##                                  NA's   :3499                                  
    ##    NONBIOKIDS         MARSTAT         LMARSTAT         RMARIT      
    ##  Min.   :0.00000   Min.   :1.000   Min.   :3.000   Min.   :0.0000  
    ##  1st Qu.:0.00000   1st Qu.:1.000   1st Qu.:6.000   1st Qu.:0.0000  
    ##  Median :0.00000   Median :3.000   Median :6.000   Median :0.0000  
    ##  Mean   :0.05262   Mean   :2.273   Mean   :5.845   Mean   :0.4832  
    ##  3rd Qu.:0.00000   3rd Qu.:3.000   3rd Qu.:6.000   3rd Qu.:1.0000  
    ##  Max.   :2.00000   Max.   :8.000   Max.   :9.000   Max.   :2.0000  
    ##                                    NA's   :1402                    
    ##     EVRMARRY         SSMARCOH           WOMREL         EARNHS_Y   
    ##  Min.   :0.0000   Min.   :0.00000   Min.   :1.000   Min.   :1988  
    ##  1st Qu.:0.0000   1st Qu.:0.00000   1st Qu.:1.000   1st Qu.:2001  
    ##  Median :0.0000   Median :0.00000   Median :1.000   Median :2008  
    ##  Mean   :0.3715   Mean   :0.02471   Mean   :1.205   Mean   :2180  
    ##  3rd Qu.:1.0000   3rd Qu.:0.00000   3rd Qu.:1.000   3rd Qu.:2015  
    ##  Max.   :1.0000   Max.   :2.00000   Max.   :2.000   Max.   :9999  
    ##                                     NA's   :2760    NA's   :901   
    ##    MYSCHOL_Y       EARNBA_Y       WTHPARNW         ONOWN          ONOWN18     
    ##  Min.   :2014   Min.   :1994   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:2022   1st Qu.:2005   1st Qu.:2.000   1st Qu.:5.000   1st Qu.:5.000  
    ##  Median :2023   Median :2011   Median :2.000   Median :5.000   Median :5.000  
    ##  Mean   :2022   Mean   :2036   Mean   :1.839   Mean   :4.523   Mean   :4.523  
    ##  3rd Qu.:2023   3rd Qu.:2016   3rd Qu.:2.000   3rd Qu.:5.000   3rd Qu.:5.000  
    ##  Max.   :2023   Max.   :9999   Max.   :2.000   Max.   :9.000   Max.   :9.000  
    ##  NA's   :4096   NA's   :2833                   NA's   :1                      
    ##      INTACT         PARMARR        INTACT18        LVSIT14F        LVSIT14M    
    ##  Min.   :1.000   Min.   :1.00   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:1.00   1st Qu.:1.000   1st Qu.:1.000   1st Qu.:1.000  
    ##  Median :1.000   Median :1.00   Median :1.000   Median :1.000   Median :2.000  
    ##  Mean   :2.071   Mean   :1.87   Mean   :1.308   Mean   :1.365   Mean   :2.381  
    ##  3rd Qu.:5.000   3rd Qu.:1.00   3rd Qu.:2.000   3rd Qu.:2.000   3rd Qu.:3.000  
    ##  Max.   :8.000   Max.   :9.00   Max.   :9.000   Max.   :9.000   Max.   :9.000  
    ##  NA's   :178                                    NA's   :3076    NA's   :3076   
    ##     WOMRASDU        MOMWORKD        MANRASDU        FOSTEREV    
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:1.000   1st Qu.:1.000   1st Qu.:5.000  
    ##  Median :1.000   Median :1.000   Median :2.000   Median :5.000  
    ##  Mean   :1.354   Mean   :1.992   Mean   :2.297   Mean   :4.912  
    ##  3rd Qu.:2.000   3rd Qu.:3.000   3rd Qu.:4.000   3rd Qu.:5.000  
    ##  Max.   :9.000   Max.   :9.000   Max.   :9.000   Max.   :9.000  
    ##  NA's   :3076    NA's   :55      NA's   :3076                   
    ##     MNYFSTER        DURFSTER        AGEFSTER        EVCOHAB1   
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.00  
    ##  1st Qu.:1.000   1st Qu.:1.500   1st Qu.:1.500   1st Qu.:5.00  
    ##  Median :2.000   Median :2.000   Median :2.000   Median :5.00  
    ##  Mean   :2.045   Mean   :2.252   Mean   :2.595   Mean   :4.18  
    ##  3rd Qu.:3.000   3rd Qu.:3.000   3rd Qu.:3.000   3rd Qu.:5.00  
    ##  Max.   :9.000   Max.   :9.000   Max.   :9.000   Max.   :9.00  
    ##  NA's   :4260    NA's   :4260    NA's   :4260    NA's   :2810  
    ##     NUMCOH1          EVCOHAB2        NUMCOH2          EVRCOHAB     
    ##  Min.   : 1.000   Min.   :1.000   Min.   : 1.000   Min.   :0.0000  
    ##  1st Qu.: 1.000   1st Qu.:5.000   1st Qu.: 1.000   1st Qu.:0.0000  
    ##  Median : 1.000   Median :5.000   Median : 1.000   Median :0.0000  
    ##  Mean   : 3.045   Mean   :4.213   Mean   : 2.771   Mean   :0.2677  
    ##  3rd Qu.: 2.000   3rd Qu.:5.000   3rd Qu.: 2.000   3rd Qu.:1.0000  
    ##  Max.   :99.000   Max.   :9.000   Max.   :99.000   Max.   :1.0000  
    ##  NA's   :3993     NA's   :2007    NA's   :3584                     
    ##     NUMCOHAB         MARSTATB       EVCOHABB       NUMCOHB         FMARIT     
    ##  Min.   : 0.000   Min.   :3.00   Min.   :1.00   Min.   :1      Min.   :0.000  
    ##  1st Qu.: 1.000   1st Qu.:6.00   1st Qu.:5.00   1st Qu.:1      1st Qu.:1.000  
    ##  Median : 1.000   Median :6.00   Median :5.00   Median :1      Median :5.000  
    ##  Mean   : 2.744   Mean   :6.05   Mean   :4.77   Mean   :1      Mean   :3.618  
    ##  3rd Qu.: 2.000   3rd Qu.:6.00   3rd Qu.:5.00   3rd Qu.:1      3rd Qu.:5.000  
    ##  Max.   :99.000   Max.   :9.00   Max.   :8.00   Max.   :1      Max.   :5.000  
    ##  NA's   :3183     NA's   :4331   NA's   :4297   NA's   :4366                  
    ##     EVERSEX         RHADSEX          YNOSEX         TALKPAR1    
    ##  Min.   :1.000   Min.   :0.000   Min.   :1.000   Min.   : 1.00  
    ##  1st Qu.:1.000   1st Qu.:1.000   1st Qu.:3.000   1st Qu.: 1.00  
    ##  Median :5.000   Median :1.000   Median :4.000   Median : 4.00  
    ##  Mean   :3.114   Mean   :1.215   Mean   :4.025   Mean   :28.13  
    ##  3rd Qu.:5.000   3rd Qu.:1.000   3rd Qu.:6.000   3rd Qu.:95.00  
    ##  Max.   :9.000   Max.   :2.000   Max.   :9.000   Max.   :99.00  
    ##  NA's   :2413                    NA's   :3396    NA's   :3215   
    ##     TALKPAR2        TALKPAR3        TALKPAR4        TALKPAR5    
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:2.000   1st Qu.:3.000   1st Qu.:4.000   1st Qu.:5.000  
    ##  Median :3.000   Median :4.000   Median :4.000   Median :5.000  
    ##  Mean   :3.379   Mean   :3.922   Mean   :4.529   Mean   :4.798  
    ##  3rd Qu.:4.000   3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:6.000  
    ##  Max.   :7.000   Max.   :7.000   Max.   :7.000   Max.   :7.000  
    ##  NA's   :3693    NA's   :3794    NA's   :3908    NA's   :4009   
    ##     TALKPAR6        TALKPAR7         SEDNO          SEDNOLC1    
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:5.750   1st Qu.:6.000   1st Qu.:1.000   1st Qu.:1.000  
    ##  Median :6.000   Median :7.000   Median :1.000   Median :1.000  
    ##  Mean   :5.307   Mean   :5.892   Mean   :2.092   Mean   :1.153  
    ##  3rd Qu.:6.000   3rd Qu.:7.000   3rd Qu.:5.000   3rd Qu.:1.000  
    ##  Max.   :7.000   Max.   :7.000   Max.   :9.000   Max.   :9.000  
    ##  NA's   :4091    NA's   :4214    NA's   :3215    NA's   :3519   
    ##     SEDNOLC2        SEDNOLC3        SEDNOLC4        SEDNOG      
    ##  Min.   :1.000   Min.   :2.000   Min.   :4      Min.   : 1.000  
    ##  1st Qu.:2.000   1st Qu.:3.000   1st Qu.:4      1st Qu.: 6.000  
    ##  Median :2.000   Median :3.000   Median :4      Median : 7.000  
    ##  Mean   :2.269   Mean   :3.222   Mean   :4      Mean   : 8.826  
    ##  3rd Qu.:3.000   3rd Qu.:4.000   3rd Qu.:4      3rd Qu.: 9.000  
    ##  Max.   :4.000   Max.   :4.000   Max.   :4      Max.   :99.000  
    ##  NA's   :4241    NA's   :4353    NA's   :4369   NA's   :3519    
    ##     SEDNOSX          SEDBC          SEDBCLC1        SEDBCLC2        SEDBCLC3   
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :3.0   
    ##  1st Qu.:1.000   1st Qu.:1.000   1st Qu.:1.000   1st Qu.:2.000   1st Qu.:4.0   
    ##  Median :1.000   Median :1.000   Median :1.000   Median :3.000   Median :4.0   
    ##  Mean   :1.104   Mean   :2.513   Mean   :1.167   Mean   :2.892   Mean   :3.8   
    ##  3rd Qu.:1.000   3rd Qu.:5.000   3rd Qu.:1.000   3rd Qu.:4.000   3rd Qu.:4.0   
    ##  Max.   :8.000   Max.   :9.000   Max.   :9.000   Max.   :4.000   Max.   :4.0   
    ##  NA's   :3987    NA's   :3215    NA's   :3641    NA's   :4306    NA's   :4366  
    ##  SEDBCLC4           SEDBCG         SEDBCSX         SEDWHBC         SEDWHLC1    
    ##  Mode:logical   Min.   : 2.00   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  NA's:4371      1st Qu.: 6.00   1st Qu.:1.000   1st Qu.:1.000   1st Qu.:1.000  
    ##                 Median : 8.00   Median :1.000   Median :5.000   Median :1.000  
    ##                 Mean   : 9.09   Mean   :1.113   Mean   :3.179   Mean   :1.377  
    ##                 3rd Qu.: 9.00   3rd Qu.:1.000   3rd Qu.:5.000   3rd Qu.:1.000  
    ##                 Max.   :99.00   Max.   :9.000   Max.   :9.000   Max.   :9.000  
    ##                 NA's   :3641    NA's   :4016    NA's   :3215    NA's   :3835   
    ##     SEDWHLC2        SEDWHLC3     SEDWHLC4          SEDWHBCG        SEDWBCSX   
    ##  Min.   :1.000   Min.   :3.000   Mode:logical   Min.   : 3.00   Min.   :1.00  
    ##  1st Qu.:2.000   1st Qu.:3.000   NA's:4371      1st Qu.: 7.00   1st Qu.:1.00  
    ##  Median :3.000   Median :3.000                  Median : 8.00   Median :1.00  
    ##  Mean   :2.909   Mean   :3.333                  Mean   :10.94   Mean   :1.17  
    ##  3rd Qu.:4.000   3rd Qu.:3.750                  3rd Qu.: 9.00   3rd Qu.:1.00  
    ##  Max.   :4.000   Max.   :4.000                  Max.   :99.00   Max.   :9.00  
    ##  NA's   :4316    NA's   :4365                   NA's   :3835    NA's   :4089  
    ##     SEDCOND        SEDCONLC1       SEDCONLC2       SEDCONLC3     SEDCONLC4     
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000   Mode:logical  
    ##  1st Qu.:1.000   1st Qu.:1.000   1st Qu.:2.000   1st Qu.:2.000   NA's:4371     
    ##  Median :1.000   Median :1.000   Median :4.000   Median :3.000                 
    ##  Mean   :2.651   Mean   :1.329   Mean   :3.158   Mean   :2.667                 
    ##  3rd Qu.:5.000   3rd Qu.:1.000   3rd Qu.:4.000   3rd Qu.:3.500                 
    ##  Max.   :9.000   Max.   :9.000   Max.   :4.000   Max.   :4.000                 
    ##  NA's   :3215    NA's   :3687    NA's   :4314    NA's   :4368                  
    ##     SEDCONDG         SEDCONSX         SEDSTD        SEDSTDLC1    
    ##  Min.   : 1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.: 7.000   1st Qu.:1.000   1st Qu.:1.000   1st Qu.:1.000  
    ##  Median : 8.000   Median :1.000   Median :1.000   Median :1.000  
    ##  Mean   : 9.965   Mean   :1.118   Mean   :1.698   Mean   :1.161  
    ##  3rd Qu.: 9.000   3rd Qu.:1.000   3rd Qu.:1.000   3rd Qu.:1.000  
    ##  Max.   :99.000   Max.   :9.000   Max.   :9.000   Max.   :9.000  
    ##  NA's   :3687     NA's   :4015    NA's   :3215    NA's   :3411   
    ##    SEDSTDLC2       SEDSTDLC3       SEDSTDLC4       SEDSTDG      
    ##  Min.   :1.000   Min.   :3.000   Min.   :4      Min.   : 1.000  
    ##  1st Qu.:2.000   1st Qu.:3.000   1st Qu.:4      1st Qu.: 6.000  
    ##  Median :4.000   Median :4.000   Median :4      Median : 8.000  
    ##  Mean   :3.047   Mean   :3.571   Mean   :4      Mean   : 9.248  
    ##  3rd Qu.:4.000   3rd Qu.:4.000   3rd Qu.:4      3rd Qu.: 9.000  
    ##  Max.   :4.000   Max.   :4.000   Max.   :4      Max.   :99.000  
    ##  NA's   :4286    NA's   :4364    NA's   :4370   NA's   :3411    
    ##     SEDSTDSX         SEDHIV        SEDHIVLC1       SEDHIVLC2       SEDHIVLC3   
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :2.0   
    ##  1st Qu.:1.000   1st Qu.:1.000   1st Qu.:1.000   1st Qu.:2.000   1st Qu.:3.0   
    ##  Median :1.000   Median :1.000   Median :1.000   Median :3.000   Median :3.0   
    ##  Mean   :1.081   Mean   :2.088   Mean   :1.192   Mean   :2.922   Mean   :3.3   
    ##  3rd Qu.:1.000   3rd Qu.:5.000   3rd Qu.:1.000   3rd Qu.:4.000   3rd Qu.:4.0   
    ##  Max.   :9.000   Max.   :9.000   Max.   :9.000   Max.   :4.000   Max.   :4.0   
    ##  NA's   :3929    NA's   :3215    NA's   :3523    NA's   :4294    NA's   :4361  
    ##    SEDHIVLC4       SEDHIVG          SEDHIVSX        SEDABST        SEDABLC1    
    ##  Min.   :1      Min.   : 1.000   Min.   :1.000   Min.   :1.00   Min.   :1.000  
    ##  1st Qu.:1      1st Qu.: 7.000   1st Qu.:1.000   1st Qu.:1.00   1st Qu.:1.000  
    ##  Median :1      Median : 8.000   Median :1.000   Median :1.00   Median :2.000  
    ##  Mean   :1      Mean   : 9.051   Mean   :1.093   Mean   :2.92   Mean   :1.867  
    ##  3rd Qu.:1      3rd Qu.: 9.000   3rd Qu.:1.000   3rd Qu.:5.00   3rd Qu.:2.000  
    ##  Max.   :1      Max.   :99.000   Max.   :9.000   Max.   :9.00   Max.   :9.000  
    ##  NA's   :4370   NA's   :3523     NA's   :3972    NA's   :3215   NA's   :3760   
    ##     SEDABLC2        SEDABLC3       SEDABLC4       SEDABSTG        SEDABSSX    
    ##  Min.   :1.000   Min.   :2.00   Min.   :1.0    Min.   : 1.00   Min.   :1.000  
    ##  1st Qu.:2.000   1st Qu.:3.00   1st Qu.:2.5    1st Qu.: 6.00   1st Qu.:1.000  
    ##  Median :2.000   Median :4.00   Median :4.0    Median : 7.00   Median :1.000  
    ##  Mean   :2.157   Mean   :3.52   Mean   :3.0    Mean   :14.56   Mean   :1.161  
    ##  3rd Qu.:2.000   3rd Qu.:4.00   3rd Qu.:4.0    3rd Qu.: 9.00   3rd Qu.:1.000  
    ##  Max.   :4.000   Max.   :4.00   Max.   :4.0    Max.   :99.00   Max.   :9.000  
    ##  NA's   :4250    NA's   :4346   NA's   :4368   NA's   :3760    NA's   :4073   
    ##     EVEROPER        TYPEOPER        VASEC_Y        PLCSTROP        RVRSVAS     
    ##  Min.   :1.000   Min.   :1.000   Min.   :1984   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:5.000   1st Qu.:1.000   1st Qu.:2013   1st Qu.:1.000   1st Qu.:5.000  
    ##  Median :5.000   Median :1.000   Median :2018   Median :1.000   Median :5.000  
    ##  Mean   :4.813   Mean   :1.085   Mean   :2016   Mean   :2.426   Mean   :4.888  
    ##  3rd Qu.:5.000   3rd Qu.:1.000   3rd Qu.:2021   3rd Qu.:5.000   3rd Qu.:5.000  
    ##  Max.   :9.000   Max.   :8.000   Max.   :2023   Max.   :6.000   Max.   :5.000  
    ##                  NA's   :4113    NA's   :4114   NA's   :4120    NA's   :4120   
    ##     VASREV_Y       RSURGSTR         FATHPOSS        FATHDIFF    
    ##  Min.   :1985   Min.   :0.0000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:2005   1st Qu.:0.0000   1st Qu.:1.000   1st Qu.:5.000  
    ##  Median :2006   Median :0.0000   Median :1.000   Median :5.000  
    ##  Mean   :2008   Mean   :0.0572   Mean   :1.398   Mean   :4.912  
    ##  3rd Qu.:2018   3rd Qu.:0.0000   3rd Qu.:1.000   3rd Qu.:5.000  
    ##  Max.   :2019   Max.   :1.0000   Max.   :9.000   Max.   :9.000  
    ##  NA's   :4364                    NA's   :251     NA's   :502    
    ##     RSTRSTAT         SXMON12         SEXSTAT        P12MOCONO    
    ##  Min.   :0.0000   Min.   :1.000   Min.   :0.000   Min.   :1.000  
    ##  1st Qu.:0.0000   1st Qu.:1.000   1st Qu.:2.000   1st Qu.:1.000  
    ##  Median :0.0000   Median :1.000   Median :6.000   Median :1.000  
    ##  Mean   :0.1725   Mean   :2.132   Mean   :3.949   Mean   :1.727  
    ##  3rd Qu.:0.0000   3rd Qu.:5.000   3rd Qu.:6.000   3rd Qu.:1.000  
    ##  Max.   :2.0000   Max.   :9.000   Max.   :6.000   Max.   :5.000  
    ##                   NA's   :3690    NA's   :22      NA's   :4349   
    ##     P12MOCON        SEXFREQ          CONFREQ           P1RLTN1     
    ##  Min.   :1.000   Min.   :  0.00   Min.   :  0.000   Min.   :1.000  
    ##  1st Qu.:2.000   1st Qu.:  1.00   1st Qu.:  0.000   1st Qu.:1.000  
    ##  Median :5.000   Median :  3.00   Median :  0.000   Median :1.000  
    ##  Mean   :3.777   Mean   : 30.62   Mean   :  5.289   Mean   :1.646  
    ##  3rd Qu.:5.000   3rd Qu.:  7.00   3rd Qu.:  1.000   3rd Qu.:1.000  
    ##  Max.   :9.000   Max.   :999.00   Max.   :999.000   Max.   :9.000  
    ##  NA's   :1617    NA's   :1595     NA's   :2332      NA's   :2756   
    ##    P1CURRWIFE      P1CURRSEP        P1RLTN2       P1COHABIT    
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.00   Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:1.000   1st Qu.:1.00   1st Qu.:1.000  
    ##  Median :1.000   Median :1.000   Median :1.00   Median :1.000  
    ##  Mean   :1.006   Mean   :1.364   Mean   :2.59   Mean   :1.034  
    ##  3rd Qu.:1.000   3rd Qu.:1.000   3rd Qu.:5.00   3rd Qu.:1.000  
    ##  Max.   :5.000   Max.   :5.000   Max.   :8.00   Max.   :5.000  
    ##  NA's   :3063    NA's   :4360    NA's   :3454   NA's   :4021   
    ##    P1SXLAST_M       P1SXLAST_Y      CMLSXP1        P2RLTN1        P2CURRWIFE  
    ##  Min.   : 1.000   Min.   :1986   Min.   :1043   Min.   :1.000   Min.   :1     
    ##  1st Qu.: 4.000   1st Qu.:2022   1st Qu.:1468   1st Qu.:5.000   1st Qu.:1     
    ##  Median : 7.000   Median :2022   Median :1476   Median :5.000   Median :1     
    ##  Mean   : 7.995   Mean   :2131   Mean   :1581   Mean   :4.767   Mean   :1     
    ##  3rd Qu.: 9.000   3rd Qu.:2023   3rd Qu.:1482   3rd Qu.:5.000   3rd Qu.:1     
    ##  Max.   :99.000   Max.   :9999   Max.   :9999   Max.   :9.000   Max.   :1     
    ##  NA's   :1031     NA's   :1031   NA's   :1031   NA's   :4285    NA's   :4370  
    ##    P2CURRSEP        P2RLTN2        P2COHABIT      P2SXLAST_M     P2SXLAST_Y  
    ##  Min.   :1.000   Min.   :1.000   Min.   :5      Min.   : 1     Min.   :2014  
    ##  1st Qu.:1.000   1st Qu.:5.000   1st Qu.:5      1st Qu.: 4     1st Qu.:2022  
    ##  Median :1.000   Median :5.000   Median :5      Median : 7     Median :2022  
    ##  Mean   :2.333   Mean   :4.082   Mean   :5      Mean   : 9     Mean   :2222  
    ##  3rd Qu.:3.000   3rd Qu.:5.000   3rd Qu.:5      3rd Qu.:10     3rd Qu.:2023  
    ##  Max.   :5.000   Max.   :9.000   Max.   :5      Max.   :99     Max.   :9999  
    ##  NA's   :4368    NA's   :4176    NA's   :4369   NA's   :3933   NA's   :3933  
    ##     CMLSXP2        P3RLTN1        P3CURRWIFE     P3CURRSEP       P3RLTN2     
    ##  Min.   :1375   Min.   :1.000   Min.   :1      Min.   :1      Min.   :1.000  
    ##  1st Qu.:1468   1st Qu.:5.000   1st Qu.:1      1st Qu.:1      1st Qu.:5.000  
    ##  Median :1474   Median :5.000   Median :1      Median :1      Median :5.000  
    ##  Mean   :1687   Mean   :4.644   Mean   :1      Mean   :1      Mean   :4.611  
    ##  3rd Qu.:1479   3rd Qu.:5.000   3rd Qu.:1      3rd Qu.:1      3rd Qu.:5.000  
    ##  Max.   :9999   Max.   :9.000   Max.   :1      Max.   :1      Max.   :9.000  
    ##  NA's   :3933   NA's   :4326    NA's   :4370   NA's   :4370   NA's   :4258   
    ##    P3COHABIT      P3SXLAST_M      P3SXLAST_Y      CMLSXP3       P1RELATION   
    ##  Min.   :1      Min.   : 1.00   Min.   :2014   Min.   :1369   Min.   :1.000  
    ##  1st Qu.:1      1st Qu.: 4.00   1st Qu.:2022   1st Qu.:1468   1st Qu.:1.000  
    ##  Median :1      Median : 7.00   Median :2022   Median :1474   Median :4.000  
    ##  Mean   :1      Mean   :10.04   Mean   :2489   Mean   :1971   Mean   :3.638  
    ##  3rd Qu.:1      3rd Qu.:11.00   3rd Qu.:2023   3rd Qu.:1479   3rd Qu.:6.000  
    ##  Max.   :1      Max.   :99.00   Max.   :9999   Max.   :9999   Max.   :9.000  
    ##  NA's   :4370   NA's   :4132    NA's   :4132   NA's   :4132   NA's   :1031   
    ##    P2RELATION      P3RELATION        FIRST         MARRDATE_Y      HISAGEM     
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1992   Min.   :16.00  
    ##  1st Qu.:6.000   1st Qu.:6.000   1st Qu.:2.000   1st Qu.:2009   1st Qu.:25.00  
    ##  Median :6.000   Median :6.000   Median :2.000   Median :2014   Median :28.00  
    ##  Mean   :5.874   Mean   :5.904   Mean   :2.368   Mean   :2065   Mean   :29.16  
    ##  3rd Qu.:6.000   3rd Qu.:6.000   3rd Qu.:2.500   3rd Qu.:2018   3rd Qu.:33.00  
    ##  Max.   :9.000   Max.   :9.000   Max.   :5.000   Max.   :9999   Max.   :98.00  
    ##  NA's   :3933    NA's   :4132    NA's   :4352    NA's   :2975   NA's   :2975   
    ##     LIVTOGSP      STRTSPCP_Y      HISAGEC         CMSTRTSP       ENGATHEN    
    ##  Min.   :1.00   Min.   :1992   Min.   :14.00   Min.   :1992   Min.   :1.000  
    ##  1st Qu.:1.00   1st Qu.:2009   1st Qu.:23.00   1st Qu.:2008   1st Qu.:3.000  
    ##  Median :1.00   Median :2014   Median :26.00   Median :2014   Median :3.000  
    ##  Mean   :2.39   Mean   :2133   Mean   :27.93   Mean   :2101   Mean   :3.571  
    ##  3rd Qu.:5.00   3rd Qu.:2019   3rd Qu.:31.00   3rd Qu.:2019   3rd Qu.:5.000  
    ##  Max.   :9.00   Max.   :9999   Max.   :98.00   Max.   :9999   Max.   :9.000  
    ##  NA's   :2975   NA's   :3041   NA's   :3041    NA's   :2566   NA's   :3041   
    ##     WILLMARR        CSPAGE          CSPEDUCN        CSPBORN     
    ##  Min.   :1.00   Min.   : 1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:1.00   1st Qu.: 4.000   1st Qu.:3.000   1st Qu.:1.000  
    ##  Median :1.00   Median : 5.000   Median :5.000   Median :5.000  
    ##  Mean   :1.76   Mean   : 5.773   Mean   :4.312   Mean   :4.008  
    ##  3rd Qu.:2.00   3rd Qu.: 6.000   3rd Qu.:6.000   3rd Qu.:5.000  
    ##  Max.   :9.00   Max.   :99.000   Max.   :9.000   Max.   :9.000  
    ##  NA's   :3962   NA's   :2566     NA's   :2566    NA's   :2566   
    ##     CSPMARBF        SSKIDTOG       NSSKIDTOG       SSKIDTOG18   
    ##  Min.   :1.000   Min.   :1.000   Min.   : 1.00   Min.   : 0.00  
    ##  1st Qu.:5.000   1st Qu.:5.000   1st Qu.: 2.25   1st Qu.: 2.00  
    ##  Median :5.000   Median :5.000   Median : 4.50   Median : 4.50  
    ##  Mean   :4.481   Mean   :4.676   Mean   :44.56   Mean   :44.39  
    ##  3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:97.00   3rd Qu.:97.00  
    ##  Max.   :9.000   Max.   :7.000   Max.   :97.00   Max.   :97.00  
    ##  NA's   :2566    NA's   :4297    NA's   :4353    NA's   :4353   
    ##    CWPSX1WN_M       CWPSX1WN_Y      CMFSXCWP       CWPSX1AG       AGEFSXCWP    
    ##  Min.   : 1.000   Min.   :1989   Min.   :1075   Min.   :15.00   Min.   :14.00  
    ##  1st Qu.: 4.000   1st Qu.:2007   1st Qu.:1292   1st Qu.:20.00   1st Qu.:21.00  
    ##  Median : 7.000   Median :2013   Median :1357   Median :24.00   Median :25.00  
    ##  Mean   : 9.626   Mean   :2201   Mean   :1550   Mean   :32.34   Mean   :26.75  
    ##  3rd Qu.:11.000   3rd Qu.:2017   3rd Qu.:1415   3rd Qu.:31.00   3rd Qu.:30.00  
    ##  Max.   :99.000   Max.   :9999   Max.   :9999   Max.   :99.00   Max.   :99.00  
    ##  NA's   :2643     NA's   :2643   NA's   :2643   NA's   :4178    NA's   :2643   
    ##     CWPSX1RL         CWPFUSE        CWPFMET01        CWPFMET02     
    ##  Min.   : 1.000   Min.   :1.000   Min.   : 1.000   Min.   : 1.000  
    ##  1st Qu.: 5.000   1st Qu.:1.000   1st Qu.: 1.000   1st Qu.: 2.000  
    ##  Median : 5.000   Median :1.000   Median : 1.000   Median : 4.000  
    ##  Mean   : 5.736   Mean   :2.194   Mean   : 2.268   Mean   : 4.002  
    ##  3rd Qu.: 6.000   3rd Qu.:5.000   3rd Qu.: 2.000   3rd Qu.: 4.000  
    ##  Max.   :99.000   Max.   :9.000   Max.   :99.000   Max.   :12.000  
    ##  NA's   :2643     NA's   :2643    NA's   :3141     NA's   :3941    
    ##    CWPFMET03        CWPFMET04        CWPFMET05       CWPOPSTR    
    ##  Min.   : 1.000   Min.   : 5.000   Min.   :12     Min.   :1.000  
    ##  1st Qu.: 4.000   1st Qu.: 6.500   1st Qu.:12     1st Qu.:5.000  
    ##  Median : 4.000   Median : 8.000   Median :12     Median :5.000  
    ##  Mean   : 5.407   Mean   : 8.167   Mean   :12     Mean   :4.632  
    ##  3rd Qu.: 7.500   3rd Qu.:10.250   3rd Qu.:12     3rd Qu.:5.000  
    ##  Max.   :12.000   Max.   :11.000   Max.   :12     Max.   :9.000  
    ##  NA's   :4312     NA's   :4365     NA's   :4370   NA's   :2652   
    ##     CWPREVST        PSURGSTR         CWPPOSS         CWPDIFF     
    ##  Min.   : 1.00   Min.   :0.0000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.: 2.00   1st Qu.:0.0000   1st Qu.:1.000   1st Qu.:5.000  
    ##  Median : 2.00   Median :0.0000   Median :1.000   Median :5.000  
    ##  Mean   :27.42   Mean   :0.1032   Mean   :1.534   Mean   :4.549  
    ##  3rd Qu.:96.00   3rd Qu.:0.0000   3rd Qu.:1.000   3rd Qu.:5.000  
    ##  Max.   :99.00   Max.   :1.0000   Max.   :9.000   Max.   :9.000  
    ##  NA's   :4190    NA's   :2637     NA's   :2816    NA's   :2986   
    ##     PSTRSTAT        CWPLSXWN_M      CWPLSXWN_Y      CMLSXCWP       CWPLUSE1    
    ##  Min.   :0.0000   Min.   : 1.00   Min.   :2002   Min.   :1177   Min.   :1.000  
    ##  1st Qu.:0.0000   1st Qu.: 4.00   1st Qu.:2022   1st Qu.:1472   1st Qu.:1.000  
    ##  Median :0.0000   Median : 8.00   Median :2022   Median :1477   Median :5.000  
    ##  Mean   :0.2993   Mean   :17.22   Mean   :3113   Mean   :1613   Mean   :3.736  
    ##  3rd Qu.:0.0000   3rd Qu.:12.00   3rd Qu.:2023   3rd Qu.:1482   3rd Qu.:5.000  
    ##  Max.   :2.0000   Max.   :99.00   Max.   :9999   Max.   :9999   Max.   :9.000  
    ##  NA's   :2637     NA's   :4298    NA's   :4298   NA's   :2644   NA's   :2643   
    ##    CWPLMET11        CWPLMET12        CWPLMET13      CWPLMET14   
    ##  Min.   : 1.000   Min.   : 1.000   Min.   :2      Min.   :10    
    ##  1st Qu.: 1.000   1st Qu.: 2.000   1st Qu.:2      1st Qu.:10    
    ##  Median : 2.000   Median : 2.000   Median :2      Median :10    
    ##  Mean   : 2.591   Mean   : 3.129   Mean   :2      Mean   :10    
    ##  3rd Qu.: 3.000   3rd Qu.: 3.000   3rd Qu.:2      3rd Qu.:10    
    ##  Max.   :99.000   Max.   :10.000   Max.   :2      Max.   :10    
    ##  NA's   :3811     NA's   :4340     NA's   :4370   NA's   :4370  
    ##     CWPLUSE2       DKCWPLUSE      CWPLMET201       CWPLMET202      CWPLMET203  
    ##  Min.   :1.000   Min.   :1.00   Min.   : 4.000   Min.   : 7.00   Min.   :6     
    ##  1st Qu.:1.000   1st Qu.:1.75   1st Qu.: 4.000   1st Qu.: 9.50   1st Qu.:6     
    ##  Median :5.000   Median :5.50   Median : 7.000   Median :10.50   Median :6     
    ##  Mean   :3.823   Mean   :5.25   Mean   : 7.715   Mean   :10.12   Mean   :6     
    ##  3rd Qu.:5.000   3rd Qu.:9.00   3rd Qu.:11.000   3rd Qu.:11.25   3rd Qu.:6     
    ##  Max.   :9.000   Max.   :9.00   Max.   :99.000   Max.   :12.00   Max.   :6     
    ##  NA's   :2643    NA's   :4367   NA's   :3848     NA's   :4363    NA's   :4370  
    ##    CWPLSXUSE         CWPRECBC       CWPALLBC01      CWPALLBC02    
    ##  Min.   :0.0000   Min.   :1.000   Min.   : 1.00   Min.   : 1.000  
    ##  1st Qu.:0.0000   1st Qu.:5.000   1st Qu.: 1.00   1st Qu.: 2.000  
    ##  Median :1.0000   Median :5.000   Median : 2.00   Median : 3.000  
    ##  Mean   :0.5242   Mean   :4.218   Mean   : 4.84   Mean   : 4.123  
    ##  3rd Qu.:1.0000   3rd Qu.:5.000   3rd Qu.: 5.00   3rd Qu.: 4.000  
    ##  Max.   :1.0000   Max.   :8.000   Max.   :99.00   Max.   :12.000  
    ##  NA's   :2637     NA's   :3615    NA's   :3318    NA's   :4047    
    ##    CWPALLBC03       CWPALLBC04      CWPALLBC05       CWPBCMST     
    ##  Min.   : 1.000   Min.   : 4.00   Min.   :11.00   Min.   : 1.000  
    ##  1st Qu.: 4.000   1st Qu.: 8.00   1st Qu.:11.25   1st Qu.: 1.000  
    ##  Median : 7.000   Median : 8.00   Median :11.50   Median : 2.000  
    ##  Mean   : 6.384   Mean   : 8.50   Mean   :11.50   Mean   : 3.985  
    ##  3rd Qu.: 8.000   3rd Qu.:10.25   3rd Qu.:11.75   3rd Qu.: 4.000  
    ##  Max.   :12.000   Max.   :12.00   Max.   :12.00   Max.   :99.000  
    ##  NA's   :4285     NA's   :4359    NA's   :4369    NA's   :4047    
    ##     CONDFREQ         CWPNOFRQ        CWPPRGNW        CWPTRYPG    
    ##  Min.   :  0.00   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:  0.00   1st Qu.:1.000   1st Qu.:5.000   1st Qu.:5.000  
    ##  Median :  0.00   Median :1.000   Median :5.000   Median :5.000  
    ##  Mean   : 33.81   Mean   :2.053   Mean   :4.756   Mean   :4.634  
    ##  3rd Qu.: 50.00   3rd Qu.:3.000   3rd Qu.:5.000   3rd Qu.:5.000  
    ##  Max.   :999.00   Max.   :8.000   Max.   :9.000   Max.   :9.000  
    ##  NA's   :3318     NA's   :3648    NA's   :3254    NA's   :3328   
    ##     CWPTRYLG         CWPCPWNT       CWPCPSON        CWPCPSNN     
    ##  Min.   :  0.00   Min.   :1.00   Min.   :1.000   Min.   :  1.00  
    ##  1st Qu.:  2.00   1st Qu.:1.00   1st Qu.:2.000   1st Qu.:  1.75  
    ##  Median :  5.00   Median :1.00   Median :2.000   Median :  2.00  
    ##  Mean   : 34.66   Mean   :1.27   Mean   :1.957   Mean   : 85.25  
    ##  3rd Qu.: 23.00   3rd Qu.:1.00   3rd Qu.:2.000   3rd Qu.:  3.00  
    ##  Max.   :999.00   Max.   :4.00   Max.   :3.000   Max.   :998.00  
    ##  NA's   :4268     NA's   :4297   NA's   :4301    NA's   :4359    
    ##    CWPCPSNMY        CWPCPHPY       MARDATEN_Y_1    AGEMARR_1    
    ##  Min.   :1.000   Min.   : 1.000   Min.   :1989   Min.   :17.00  
    ##  1st Qu.:2.000   1st Qu.: 9.000   1st Qu.:2005   1st Qu.:22.00  
    ##  Median :2.000   Median :10.000   Median :2010   Median :26.00  
    ##  Mean   :2.333   Mean   : 9.149   Mean   :2009   Mean   :27.45  
    ##  3rd Qu.:2.000   3rd Qu.:10.000   3rd Qu.:2015   3rd Qu.:30.00  
    ##  Max.   :8.000   Max.   :10.000   Max.   :2023   Max.   :46.00  
    ##  NA's   :4359    NA's   :4297     NA's   :4318   NA's   :4318   
    ##    LIVTOGN_1        AGELIV_1       CMUNIONP_1     ENGAGTHN_1      MARREND_1    
    ##  Min.   :1.000   Min.   :16.00   Min.   :1989   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:22.00   1st Qu.:2011   1st Qu.:3.000   1st Qu.:2.000  
    ##  Median :5.000   Median :26.00   Median :2016   Median :5.000   Median :2.000  
    ##  Mean   :3.396   Mean   :28.25   Mean   :2045   Mean   :4.144   Mean   :2.623  
    ##  3rd Qu.:5.000   3rd Qu.:31.00   3rd Qu.:2020   3rd Qu.:5.000   3rd Qu.:4.000  
    ##  Max.   :8.000   Max.   :99.00   Max.   :9998   Max.   :9.000   Max.   :9.000  
    ##  NA's   :4318    NA's   :4142    NA's   :4111   NA's   :4142    NA's   :4318   
    ##   ENDMARR_Y_1    STOPLIVE_Y_1      PXCURR        PXCURRPRT         PXMARRY     
    ##  Min.   :2000   Min.   :1994   Min.   :1.000   Min.   :0.0000   Min.   :1.000  
    ##  1st Qu.:2014   1st Qu.:2017   1st Qu.:1.000   1st Qu.:0.0000   1st Qu.:2.000  
    ##  Median :2020   Median :2021   Median :1.000   Median :0.0000   Median :2.000  
    ##  Mean   :2222   Mean   :2390   Mean   :2.566   Mean   :0.4286   Mean   :2.602  
    ##  3rd Qu.:2022   3rd Qu.:2022   3rd Qu.:5.000   3rd Qu.:1.0000   3rd Qu.:3.000  
    ##  Max.   :9998   Max.   :9999   Max.   :9.000   Max.   :1.0000   Max.   :9.000  
    ##  NA's   :4332   NA's   :4113   NA's   :3190    NA's   :2684     NA's   :3653   
    ##     PXLRUSE        PXLRMETH1        PXLRMETH2        PXLRMETH3    
    ##  Min.   :1.000   Min.   : 1.000   Min.   : 1.000   Min.   : 3.00  
    ##  1st Qu.:1.000   1st Qu.: 1.000   1st Qu.: 2.000   1st Qu.: 4.75  
    ##  Median :1.000   Median : 1.000   Median : 2.000   Median :10.00  
    ##  Mean   :2.585   Mean   : 1.689   Mean   : 2.791   Mean   : 7.90  
    ##  3rd Qu.:5.000   3rd Qu.: 1.000   3rd Qu.: 2.000   3rd Qu.:10.00  
    ##  Max.   :9.000   Max.   :98.000   Max.   :10.000   Max.   :10.00  
    ##  NA's   :2685    NA's   :3334     NA's   :4237     NA's   :4361   
    ##    PXLRMETH4       PXLPUSE       DKPXLPUSE       PXLPMETH01    
    ##  Min.   :10     Min.   :1.00   Min.   :1.000   Min.   : 4.000  
    ##  1st Qu.:10     1st Qu.:1.00   1st Qu.:1.000   1st Qu.: 4.000  
    ##  Median :10     Median :5.00   Median :2.000   Median : 4.000  
    ##  Mean   :10     Mean   :3.29   Mean   :2.816   Mean   : 8.748  
    ##  3rd Qu.:10     3rd Qu.:5.00   3rd Qu.:2.000   3rd Qu.: 9.000  
    ##  Max.   :10     Max.   :9.00   Max.   :9.000   Max.   :99.000  
    ##  NA's   :4369   NA's   :2685   NA's   :4295    NA's   :3566    
    ##    PXLPMETH02       PXLPMETH03       PXLPMETH04     PXLPMETH05  
    ##  Min.   : 4.000   Min.   : 4.000   Min.   :7      Min.   :10    
    ##  1st Qu.: 5.250   1st Qu.: 5.000   1st Qu.:7      1st Qu.:10    
    ##  Median : 7.000   Median : 6.000   Median :7      Median :10    
    ##  Mean   : 7.579   Mean   : 7.333   Mean   :7      Mean   :10    
    ##  3rd Qu.:11.000   3rd Qu.: 9.000   3rd Qu.:7      3rd Qu.:10    
    ##  Max.   :12.000   Max.   :12.000   Max.   :7      Max.   :10    
    ##  NA's   :4333     NA's   :4368     NA's   :4370   NA's   :4370  
    ##     LSXUSEP          MTONCEP         PXMTONCE        PXFRLTN1     
    ##  Min.   :0.0000   Min.   :0.000   Min.   :1.000   Min.   : 1.000  
    ##  1st Qu.:1.0000   1st Qu.:1.000   1st Qu.:1.000   1st Qu.: 5.000  
    ##  Median :1.0000   Median :1.000   Median :1.000   Median : 5.000  
    ##  Mean   :0.7645   Mean   :1.152   Mean   :1.745   Mean   : 6.853  
    ##  3rd Qu.:1.0000   3rd Qu.:1.000   3rd Qu.:1.000   3rd Qu.: 7.000  
    ##  Max.   :1.0000   Max.   :2.000   Max.   :9.000   Max.   :99.000  
    ##  NA's   :2685     NA's   :2685    NA's   :3197    NA's   :2695    
    ##      PXEDUC         PXMARBF         PXABLECH       PXSXFRST_M    
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   : 1.000  
    ##  1st Qu.:2.000   1st Qu.:5.000   1st Qu.:1.000   1st Qu.: 4.000  
    ##  Median :3.000   Median :5.000   Median :1.000   Median : 7.000  
    ##  Mean   :3.618   Mean   :4.381   Mean   :1.964   Mean   : 9.198  
    ##  3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:1.000   3rd Qu.:11.000  
    ##  Max.   :9.000   Max.   :9.000   Max.   :9.000   Max.   :99.000  
    ##  NA's   :2684    NA's   :2684    NA's   :3669    NA's   :2963    
    ##    PXSXFRST_Y       CMFSXP       AGEFSXP             PXAGFRST   
    ##  Min.   :1983   Min.   : 998   Length:4371        Min.   :14    
    ##  1st Qu.:2016   1st Qu.:1400   Class :character   1st Qu.:20    
    ##  Median :2021   Median :1453   Mode  :character   Median :25    
    ##  Mean   :2171   Mean   :1583                      Mean   :30    
    ##  3rd Qu.:2022   3rd Qu.:1469                      3rd Qu.:33    
    ##  Max.   :9999   Max.   :9999                      Max.   :99    
    ##  NA's   :2963   NA's   :2963                      NA's   :4150  
    ##     PXFRLTN2          PXFUSE        PXFMETH01        PXFMETH02     
    ##  Min.   : 1.000   Min.   :1.000   Min.   : 1.000   Min.   : 1.000  
    ##  1st Qu.: 5.000   1st Qu.:1.000   1st Qu.: 1.000   1st Qu.: 2.000  
    ##  Median : 6.000   Median :1.000   Median : 1.000   Median : 4.000  
    ##  Mean   : 6.818   Mean   :2.188   Mean   : 2.073   Mean   : 4.057  
    ##  3rd Qu.: 7.000   3rd Qu.:5.000   3rd Qu.: 2.000   3rd Qu.: 4.000  
    ##  Max.   :99.000   Max.   :9.000   Max.   :12.000   Max.   :12.000  
    ##  NA's   :2963     NA's   :2963    NA's   :3360     NA's   :4020    
    ##    PXFMETH03        PXFMETH04        PXFMETH05       PXANYUSE    
    ##  Min.   : 2.000   Min.   : 1.000   Min.   :6      Min.   :1.000  
    ##  1st Qu.: 4.000   1st Qu.: 7.000   1st Qu.:6      1st Qu.:1.000  
    ##  Median : 4.000   Median :10.000   Median :6      Median :5.000  
    ##  Mean   : 5.303   Mean   : 8.286   Mean   :6      Mean   :4.074  
    ##  3rd Qu.: 7.500   3rd Qu.:10.500   3rd Qu.:6      3rd Qu.:5.000  
    ##  Max.   :12.000   Max.   :12.000   Max.   :6      Max.   :9.000  
    ##  NA's   :4305     NA's   :4364     NA's   :4370   NA's   :4127   
    ##    PXMETHOD01       PXMETHOD02       PXMETHOD03       PXMETHOD04    
    ##  Min.   : 1.000   Min.   : 1.000   Min.   : 1.000   Min.   : 4.000  
    ##  1st Qu.: 1.000   1st Qu.: 2.000   1st Qu.: 4.000   1st Qu.: 8.000  
    ##  Median : 1.000   Median : 4.000   Median : 4.000   Median : 9.000  
    ##  Mean   : 3.278   Mean   : 3.824   Mean   : 5.764   Mean   : 9.074  
    ##  3rd Qu.: 2.000   3rd Qu.: 4.000   3rd Qu.: 8.000   3rd Qu.:11.000  
    ##  Max.   :99.000   Max.   :12.000   Max.   :12.000   Max.   :12.000  
    ##  NA's   :3526     NA's   :3922     NA's   :4223     NA's   :4344    
    ##    PXMETHOD05       PXMSTUSE         PXCONFRQ         PXNOFREQ    
    ##  Min.   : 8.00   Min.   : 1.000   Min.   :  0.00   Min.   :1.000  
    ##  1st Qu.: 8.75   1st Qu.: 1.000   1st Qu.:  0.00   1st Qu.:1.000  
    ##  Median : 9.50   Median : 2.000   Median : 50.00   Median :1.000  
    ##  Mean   : 9.50   Mean   : 3.385   Mean   : 66.33   Mean   :1.924  
    ##  3rd Qu.:10.25   3rd Qu.: 4.000   3rd Qu.:100.00   3rd Qu.:2.000  
    ##  Max.   :11.00   Max.   :98.000   Max.   :999.00   Max.   :9.000  
    ##  NA's   :4369    NA's   :3922     NA's   :3526     NA's   :3802   
    ##     PXCPREG         PXTRYING       PXTRYLONG        PXRWANT         PXRSOON    
    ##  Min.   :1.000   Min.   :1.000   Min.   : 0.00   Min.   :1.000   Min.   :1.0   
    ##  1st Qu.:5.000   1st Qu.:5.000   1st Qu.: 3.00   1st Qu.:1.000   1st Qu.:1.0   
    ##  Median :5.000   Median :5.000   Median : 6.00   Median :1.000   Median :1.5   
    ##  Mean   :4.919   Mean   :4.953   Mean   : 8.25   Mean   :1.857   Mean   :2.0   
    ##  3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:11.50   3rd Qu.:1.000   3rd Qu.:2.0   
    ##  Max.   :9.000   Max.   :9.000   Max.   :24.00   Max.   :9.000   Max.   :8.0   
    ##  NA's   :3763    NA's   :3777    NA's   :4363    NA's   :4357    NA's   :4359  
    ##     PXRSOONN       PXRSOONMY        PXCPFEEL      MARDATEN_Y_2    AGEMARR_2   
    ##  Min.   : 2.00   Min.   :1.000   Min.   : 2.00   Min.   :2012   Min.   :26    
    ##  1st Qu.: 2.75   1st Qu.:1.250   1st Qu.:10.00   1st Qu.:2014   1st Qu.:27    
    ##  Median : 5.50   Median :2.000   Median :10.00   Median :2015   Median :31    
    ##  Mean   : 6.50   Mean   :2.833   Mean   :15.36   Mean   :2016   Mean   :32    
    ##  3rd Qu.: 8.25   3rd Qu.:2.000   3rd Qu.:10.00   3rd Qu.:2020   3rd Qu.:37    
    ##  Max.   :15.00   Max.   :9.000   Max.   :99.00   Max.   :2020   Max.   :39    
    ##  NA's   :4365    NA's   :4365    NA's   :4357    NA's   :4366   NA's   :4366  
    ##    LIVTOGN_2       AGELIV_2       CMUNIONP_2     ENGAGTHN_2      MARREND_2   
    ##  Min.   :1      Min.   :15.00   Min.   :2004   Min.   :1.000   Min.   :2     
    ##  1st Qu.:1      1st Qu.:23.00   1st Qu.:2017   1st Qu.:3.000   1st Qu.:2     
    ##  Median :1      Median :25.00   Median :2020   Median :5.000   Median :3     
    ##  Mean   :1      Mean   :27.02   Mean   :2019   Mean   :4.189   Mean   :3     
    ##  3rd Qu.:1      3rd Qu.:31.00   3rd Qu.:2021   3rd Qu.:5.000   3rd Qu.:4     
    ##  Max.   :1      Max.   :45.00   Max.   :2023   Max.   :9.000   Max.   :4     
    ##  NA's   :4366   NA's   :4318    NA's   :4318   NA's   :4318    NA's   :4366  
    ##   ENDMARR_Y_2    STOPLIVE_Y_2     PXCURR2       PXCURRPRT2       PXMARRY2    
    ##  Min.   :2014   Min.   :2014   Min.   :1.00   Min.   :0.000   Min.   :1.000  
    ##  1st Qu.:2017   1st Qu.:2021   1st Qu.:5.00   1st Qu.:0.000   1st Qu.:3.000  
    ##  Median :2020   Median :2022   Median :5.00   Median :0.000   Median :4.000  
    ##  Mean   :2018   Mean   :2021   Mean   :4.43   Mean   :0.149   Mean   :3.484  
    ##  3rd Qu.:2020   3rd Qu.:2022   3rd Qu.:5.00   3rd Qu.:0.000   3rd Qu.:4.000  
    ##  Max.   :2020   Max.   :2023   Max.   :9.00   Max.   :1.000   Max.   :9.000  
    ##  NA's   :4368   NA's   :4318   NA's   :3934   NA's   :3934    NA's   :4307   
    ##     PXLRUSE2       PXLRMETH5        PXLRMETH6      PXLRMETH7     
    ##  Min.   :1.000   Min.   : 1.000   Min.   : 1.000   Mode:logical  
    ##  1st Qu.:1.000   1st Qu.: 1.000   1st Qu.: 2.000   NA's:4371     
    ##  Median :1.000   Median : 1.000   Median : 2.000                 
    ##  Mean   :2.703   Mean   : 1.336   Mean   : 2.143                 
    ##  3rd Qu.:5.000   3rd Qu.: 1.000   3rd Qu.: 2.000                 
    ##  Max.   :9.000   Max.   :10.000   Max.   :10.000                 
    ##  NA's   :3934    NA's   :4115     NA's   :4329                   
    ##  PXLRMETH8         PXLPUSE2       DKPXLPUSE2      PXLPMETH11      PXLPMETH12  
    ##  Mode:logical   Min.   :1.000   Min.   :1.000   Min.   : 4.00   Min.   : 4    
    ##  NA's:4371      1st Qu.:1.000   1st Qu.:2.000   1st Qu.: 4.00   1st Qu.: 4    
    ##                 Median :5.000   Median :2.000   Median : 4.00   Median : 8    
    ##                 Mean   :3.638   Mean   :3.182   Mean   : 7.96   Mean   : 8    
    ##                 3rd Qu.:5.000   3rd Qu.:2.000   3rd Qu.:11.00   3rd Qu.:12    
    ##                 Max.   :9.000   Max.   :9.000   Max.   :99.00   Max.   :12    
    ##                 NA's   :3934    NA's   :4349    NA's   :4198    NA's   :4367  
    ##  PXLPMETH13     PXLPMETH14     PXLPMETH15        LSXUSEP2        MTONCEP2    
    ##  Mode:logical   Mode:logical   Mode:logical   Min.   :0.000   Min.   :0.000  
    ##  NA's:4371      NA's:4371      NA's:4371      1st Qu.:0.000   1st Qu.:1.000  
    ##                                               Median :1.000   Median :1.000  
    ##                                               Mean   :0.705   Mean   :1.314  
    ##                                               3rd Qu.:1.000   3rd Qu.:2.000  
    ##                                               Max.   :1.000   Max.   :2.000  
    ##                                               NA's   :3934    NA's   :3934   
    ##    PXMTONCE2        PXFRLTN3         PXEDUC2         PXMARBF2    
    ##  Min.   :1.000   Min.   : 1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.: 6.000   1st Qu.:2.000   1st Qu.:5.000  
    ##  Median :1.000   Median : 7.000   Median :3.000   Median :5.000  
    ##  Mean   :2.487   Mean   : 6.816   Mean   :3.277   Mean   :4.266  
    ##  3rd Qu.:5.000   3rd Qu.: 7.000   3rd Qu.:5.000   3rd Qu.:5.000  
    ##  Max.   :9.000   Max.   :99.000   Max.   :9.000   Max.   :9.000  
    ##  NA's   :3987    NA's   :3936     NA's   :4306    NA's   :4262   
    ##    PXABLECH2      PXSXFRST_M2      PXSXFRST_Y2      CMFSXP2        AGEFSXP2    
    ##  Min.   :1.000   Min.   : 1.000   Min.   :1995   Min.   :1143   Min.   :13.00  
    ##  1st Qu.:1.000   1st Qu.: 3.000   1st Qu.:2020   1st Qu.:1443   1st Qu.:22.00  
    ##  Median :1.000   Median : 7.000   Median :2021   Median :1462   Median :28.00  
    ##  Mean   :2.562   Mean   : 8.845   Mean   :2209   Mean   :1649   Mean   :28.97  
    ##  3rd Qu.:5.000   3rd Qu.:10.000   3rd Qu.:2022   3rd Qu.:1472   3rd Qu.:34.00  
    ##  Max.   :9.000   Max.   :99.000   Max.   :9999   Max.   :9999   Max.   :99.00  
    ##  NA's   :4307    NA's   :4075     NA's   :4075   NA's   :4075   NA's   :4075   
    ##    PXAGFRST2       PXFRLTN4         PXFUSE2        PXFMETH14     
    ##  Min.   :17.0   Min.   : 3.000   Min.   :1.000   Min.   : 1.000  
    ##  1st Qu.:22.5   1st Qu.: 6.000   1st Qu.:1.000   1st Qu.: 1.000  
    ##  Median :27.0   Median : 7.000   Median :1.000   Median : 1.000  
    ##  Mean   :29.7   Mean   : 7.044   Mean   :2.348   Mean   : 2.025  
    ##  3rd Qu.:34.0   3rd Qu.: 7.000   3rd Qu.:5.000   3rd Qu.: 2.000  
    ##  Max.   :99.0   Max.   :98.000   Max.   :9.000   Max.   :12.000  
    ##  NA's   :4328   NA's   :4075     NA's   :4075    NA's   :4171    
    ##    PXFMETH15        PXFMETH16        PXFMETH17    PXFMETH18     
    ##  Min.   : 1.000   Min.   : 4.000   Min.   :8      Mode:logical  
    ##  1st Qu.: 2.000   1st Qu.: 4.000   1st Qu.:8      NA's:4371     
    ##  Median : 4.000   Median : 4.000   Median :8                    
    ##  Mean   : 3.905   Mean   : 6.818   Mean   :8                    
    ##  3rd Qu.: 4.000   3rd Qu.:11.000   3rd Qu.:8                    
    ##  Max.   :12.000   Max.   :12.000   Max.   :8                    
    ##  NA's   :4308     NA's   :4360     NA's   :4370                 
    ##    PXANYUSE2       PXMETHOD14       PXMETHOD15       PXMETHOD16    
    ##  Min.   :1.000   Min.   : 1.000   Min.   : 1.000   Min.   : 1.000  
    ##  1st Qu.:5.000   1st Qu.: 1.000   1st Qu.: 2.000   1st Qu.: 2.500  
    ##  Median :5.000   Median : 1.000   Median : 2.000   Median : 5.000  
    ##  Mean   :4.636   Mean   : 2.073   Mean   : 3.091   Mean   : 5.286  
    ##  3rd Qu.:5.000   3rd Qu.: 2.000   3rd Qu.: 4.000   3rd Qu.: 7.500  
    ##  Max.   :5.000   Max.   :11.000   Max.   :11.000   Max.   :11.000  
    ##  NA's   :4349    NA's   :4330     NA's   :4349     NA's   :4364    
    ##    PXMETHOD17   PXMETHOD18       PXMSTUSE2        PXCONFRQ2     
    ##  Min.   :11     Mode:logical   Min.   : 1.000   Min.   :  0.00  
    ##  1st Qu.:11     NA's:4371      1st Qu.: 1.000   1st Qu.:  0.00  
    ##  Median :11                    Median : 2.000   Median : 30.00  
    ##  Mean   :11                    Mean   : 7.045   Mean   : 58.42  
    ##  3rd Qu.:11                    3rd Qu.: 4.000   3rd Qu.:100.00  
    ##  Max.   :11                    Max.   :99.000   Max.   :999.00  
    ##  NA's   :4370                  NA's   :4349     NA's   :4095    
    ##    PXNOFREQ2        PXCPREG2       PXTRYING2    PXTRYLONG2        PXRWANT2   
    ##  Min.   :1.000   Min.   :1.000   Min.   :5      Mode:logical   Min.   :1.00  
    ##  1st Qu.:1.000   1st Qu.:5.000   1st Qu.:5      NA's:4371      1st Qu.:1.25  
    ##  Median :3.000   Median :5.000   Median :5                     Median :1.50  
    ##  Mean   :2.995   Mean   :4.852   Mean   :5                     Mean   :1.50  
    ##  3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:5                     3rd Qu.:1.75  
    ##  Max.   :8.000   Max.   :5.000   Max.   :5                     Max.   :2.00  
    ##  NA's   :4185    NA's   :4317    NA's   :4319                  NA's   :4369  
    ##     PXRSOON2    PXRSOONN2      PXRSOONMY2       PXCPFEEL2      MARDATEN_Y_3 
    ##  Min.   :2.00   Mode:logical   Mode:logical   Min.   : 9.00   Min.   :2009  
    ##  1st Qu.:2.25   NA's:4371      NA's:4371      1st Qu.: 9.25   1st Qu.:2013  
    ##  Median :2.50                                 Median : 9.50   Median :2015  
    ##  Mean   :2.50                                 Mean   : 9.50   Mean   :2015  
    ##  3rd Qu.:2.75                                 3rd Qu.: 9.75   3rd Qu.:2017  
    ##  Max.   :3.00                                 Max.   :10.00   Max.   :2020  
    ##  NA's   :4369                                 NA's   :4369    NA's   :4367  
    ##    AGEMARR_3       LIVTOGN_3       AGELIV_3       CMUNIONP_3     ENGAGTHN_3   
    ##  Min.   :28.00   Min.   :1      Min.   :18.00   Min.   :2008   Min.   :3.000  
    ##  1st Qu.:28.75   1st Qu.:1      1st Qu.:19.25   1st Qu.:2012   1st Qu.:3.000  
    ##  Median :30.50   Median :1      Median :26.50   Median :2017   Median :3.000  
    ##  Mean   :32.00   Mean   :2      Mean   :26.29   Mean   :2016   Mean   :3.571  
    ##  3rd Qu.:33.75   3rd Qu.:2      3rd Qu.:32.50   3rd Qu.:2021   3rd Qu.:4.500  
    ##  Max.   :39.00   Max.   :5      Max.   :37.00   Max.   :2023   Max.   :5.000  
    ##  NA's   :4367    NA's   :4367   NA's   :4357    NA's   :4356   NA's   :4357   
    ##    MARREND_3     ENDMARR_Y_3    STOPLIVE_Y_3     PXCURR3        PXCURRPRT3   
    ##  Min.   :2.00   Min.   :2019   Min.   :2008   Min.   :1.000   Min.   :0.000  
    ##  1st Qu.:2.00   1st Qu.:2020   1st Qu.:2020   1st Qu.:5.000   1st Qu.:0.000  
    ##  Median :3.00   Median :2021   Median :2021   Median :5.000   Median :0.000  
    ##  Mean   :4.25   Mean   :2021   Mean   :2020   Mean   :4.527   Mean   :0.131  
    ##  3rd Qu.:5.25   3rd Qu.:2022   3rd Qu.:2022   3rd Qu.:5.000   3rd Qu.:0.000  
    ##  Max.   :9.00   Max.   :2023   Max.   :2023   Max.   :8.000   Max.   :1.000  
    ##  NA's   :4367   NA's   :4369   NA's   :4357   NA's   :4134    NA's   :4134   
    ##     PXMARRY3       PXLRUSE3      PXLRMETH9       PXLRMETH10     PXLRMETH11    
    ##  Min.   :1.0    Min.   :1.00   Min.   : 1.00   Min.   : 1.000   Mode:logical  
    ##  1st Qu.:3.0    1st Qu.:1.00   1st Qu.: 1.00   1st Qu.: 2.000   NA's:4371     
    ##  Median :4.0    Median :1.00   Median : 1.00   Median : 2.000                 
    ##  Mean   :3.3    Mean   :2.73   Mean   : 1.38   Mean   : 2.368                 
    ##  3rd Qu.:4.0    3rd Qu.:5.00   3rd Qu.: 1.00   3rd Qu.: 2.000                 
    ##  Max.   :4.0    Max.   :9.00   Max.   :10.00   Max.   :10.000                 
    ##  NA's   :4341   NA's   :4134   NA's   :4234    NA's   :4352                   
    ##  PXLRMETH12        PXLPUSE3       DKPXLPUSE3     PXLPMETH21       PXLPMETH22  
    ##  Mode:logical   Min.   :1.000   Min.   :1.0    Min.   : 4.000   Min.   :7     
    ##  NA's:4371      1st Qu.:1.000   1st Qu.:2.0    1st Qu.: 4.000   1st Qu.:7     
    ##                 Median :5.000   Median :2.0    Median : 4.000   Median :7     
    ##                 Mean   :3.608   Mean   :3.3    Mean   : 8.745   Mean   :7     
    ##                 3rd Qu.:5.000   3rd Qu.:2.0    3rd Qu.: 7.000   3rd Qu.:7     
    ##                 Max.   :9.000   Max.   :9.0    Max.   :99.000   Max.   :7     
    ##                 NA's   :4134    NA's   :4361   NA's   :4277     NA's   :4370  
    ##  PXLPMETH23     PXLPMETH24     PXLPMETH25        LSXUSEP3        MTONCEP3    
    ##  Mode:logical   Mode:logical   Mode:logical   Min.   :0.000   Min.   :0.000  
    ##  NA's:4371      NA's:4371      NA's:4371      1st Qu.:0.000   1st Qu.:1.000  
    ##                                               Median :1.000   Median :1.000  
    ##                                               Mean   :0.692   Mean   :1.392  
    ##                                               3rd Qu.:1.000   3rd Qu.:2.000  
    ##                                               Max.   :1.000   Max.   :2.000  
    ##                                               NA's   :4134    NA's   :4134   
    ##    PXMTONCE3        PXFRLTN5         PXEDUC3         PXMARBF3   
    ##  Min.   :1.000   Min.   : 1.000   Min.   :1.000   Min.   :1     
    ##  1st Qu.:1.000   1st Qu.: 6.000   1st Qu.:2.000   1st Qu.:1     
    ##  Median :1.000   Median : 7.000   Median :3.000   Median :5     
    ##  Mean   :2.829   Mean   : 8.021   Mean   :3.129   Mean   :4     
    ##  3rd Qu.:5.000   3rd Qu.: 8.000   3rd Qu.:4.000   3rd Qu.:5     
    ##  Max.   :9.000   Max.   :99.000   Max.   :6.000   Max.   :9     
    ##  NA's   :4149    NA's   :4135     NA's   :4340    NA's   :4331  
    ##    PXABLECH3      PXSXFRST_M3     PXSXFRST_Y3      CMFSXP3        AGEFSXP3    
    ##  Min.   :1.000   Min.   : 1.00   Min.   :2005   Min.   :1263   Min.   :14.00  
    ##  1st Qu.:1.000   1st Qu.: 4.00   1st Qu.:2020   1st Qu.:1442   1st Qu.:22.00  
    ##  Median :1.000   Median : 7.00   Median :2021   Median :1464   Median :28.00  
    ##  Mean   :3.069   Mean   :11.99   Mean   :2251   Mean   :1694   Mean   :29.39  
    ##  3rd Qu.:5.000   3rd Qu.:12.00   3rd Qu.:2022   3rd Qu.:1472   3rd Qu.:35.00  
    ##  Max.   :9.000   Max.   :99.00   Max.   :9999   Max.   :9999   Max.   :99.00  
    ##  NA's   :4342    NA's   :4233    NA's   :4233   NA's   :4233   NA's   :4233   
    ##    PXAGFRST3        PXFRLTN6        PXFUSE3        PXFMETH27    
    ##  Min.   :15.00   Min.   :5.000   Min.   :1.000   Min.   : 1.00  
    ##  1st Qu.:24.50   1st Qu.:6.000   1st Qu.:1.000   1st Qu.: 1.00  
    ##  Median :30.00   Median :7.000   Median :1.000   Median : 1.00  
    ##  Mean   :36.11   Mean   :6.899   Mean   :2.014   Mean   : 2.34  
    ##  3rd Qu.:36.00   3rd Qu.:7.750   3rd Qu.:4.000   3rd Qu.: 2.00  
    ##  Max.   :99.00   Max.   :9.000   Max.   :5.000   Max.   :11.00  
    ##  NA's   :4344    NA's   :4233    NA's   :4233    NA's   :4268   
    ##    PXFMETH28        PXFMETH29      PXFMETH30      PXFMETH31     
    ##  Min.   : 1.000   Min.   : 1.000   Mode:logical   Mode:logical  
    ##  1st Qu.: 2.000   1st Qu.: 4.000   NA's:4371      NA's:4371     
    ##  Median : 2.500   Median : 4.000                                
    ##  Mean   : 3.353   Mean   : 4.556                                
    ##  3rd Qu.: 4.000   3rd Qu.: 4.000                                
    ##  Max.   :11.000   Max.   :11.000                                
    ##  NA's   :4337     NA's   :4362                                  
    ##    PXANYUSE3       PXMETHOD27       PXMETHOD28     PXMETHOD29    
    ##  Min.   :5.000   Min.   : 1.000   Min.   : 2.000   Mode:logical  
    ##  1st Qu.:5.000   1st Qu.: 1.000   1st Qu.: 2.500   NA's:4371     
    ##  Median :5.000   Median : 1.000   Median : 4.000                 
    ##  Mean   :5.364   Mean   : 2.765   Mean   : 4.667                 
    ##  3rd Qu.:5.000   3rd Qu.: 1.000   3rd Qu.: 4.750                 
    ##  Max.   :9.000   Max.   :11.000   Max.   :11.000                 
    ##  NA's   :4360    NA's   :4354     NA's   :4365                   
    ##  PXMETHOD30     PXMETHOD31       PXMSTUSE3      PXCONFRQ3        PXNOFREQ3    
    ##  Mode:logical   Mode:logical   Min.   :1.00   Min.   :  0.00   Min.   :1.000  
    ##  NA's:4371      NA's:4371      1st Qu.:1.25   1st Qu.:  0.00   1st Qu.:1.000  
    ##                                Median :2.00   Median : 50.00   Median :2.000  
    ##                                Mean   :2.50   Mean   : 65.05   Mean   :2.724  
    ##                                3rd Qu.:3.50   3rd Qu.:100.00   3rd Qu.:4.000  
    ##                                Max.   :5.00   Max.   :999.00   Max.   :8.000  
    ##                                NA's   :4365   NA's   :4244     NA's   :4295   
    ##     PXCPREG3       PXTRYING3    PXTRYLONG3        PXRWANT3       PXRSOON3   
    ##  Min.   :1.000   Min.   :5      Mode:logical   Min.   :1      Min.   :1.00  
    ##  1st Qu.:5.000   1st Qu.:5      NA's:4371      1st Qu.:1      1st Qu.:1.25  
    ##  Median :5.000   Median :5                     Median :1      Median :1.50  
    ##  Mean   :4.692   Mean   :5                     Mean   :1      Mean   :1.50  
    ##  3rd Qu.:5.000   3rd Qu.:5                     3rd Qu.:1      3rd Qu.:1.75  
    ##  Max.   :5.000   Max.   :5                     Max.   :1      Max.   :2.00  
    ##  NA's   :4345    NA's   :4347                  NA's   :4369   NA's   :4369  
    ##    PXRSOONN3      PXRSOONMY3     PXCPFEEL3        CURRPREG      
    ##  Min.   :2      Min.   :2      Min.   : 9.00   Min.   :0.00000  
    ##  1st Qu.:2      1st Qu.:2      1st Qu.: 9.25   1st Qu.:0.00000  
    ##  Median :2      Median :2      Median : 9.50   Median :0.00000  
    ##  Mean   :2      Mean   :2      Mean   : 9.50   Mean   :0.02013  
    ##  3rd Qu.:2      3rd Qu.:2      3rd Qu.: 9.75   3rd Qu.:0.00000  
    ##  Max.   :2      Max.   :2      Max.   :10.00   Max.   :1.00000  
    ##  NA's   :4370   NA's   :4370   NA's   :4369                     
    ##     CURRPRTS        NFORMCOHAB       FW1MARBEG_Y     FW1MARAGE    
    ##  Min.   :0.0000   Min.   :  0.000   Min.   :1989   Min.   :17.00  
    ##  1st Qu.:0.0000   1st Qu.:  0.000   1st Qu.:2001   1st Qu.:21.00  
    ##  Median :0.0000   Median :  0.000   Median :2006   Median :24.00  
    ##  Mean   :0.2526   Mean   :  3.148   Mean   :2092   Mean   :25.21  
    ##  3rd Qu.:0.0000   3rd Qu.:  0.000   3rd Qu.:2012   3rd Qu.:27.50  
    ##  Max.   :9.0000   Max.   :999.000   Max.   :9999   Max.   :99.00  
    ##                   NA's   :18        NA's   :4000   NA's   :4000   
    ##    LIVTOGN_W1      AGELIV_W1       CMUNIONW1     ENGAGTHN_W1      MARREND_W1   
    ##  Min.   :1.000   Min.   :16.00   Min.   :1988   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:20.00   1st Qu.:2000   1st Qu.:3.000   1st Qu.:2.000  
    ##  Median :1.000   Median :22.00   Median :2005   Median :3.000   Median :2.000  
    ##  Mean   :2.488   Mean   :23.12   Mean   :2117   Mean   :3.669   Mean   :2.114  
    ##  3rd Qu.:5.000   3rd Qu.:25.00   3rd Qu.:2010   3rd Qu.:5.000   3rd Qu.:2.000  
    ##  Max.   :8.000   Max.   :47.00   Max.   :9999   Max.   :9.000   Max.   :4.000  
    ##  NA's   :4000    NA's   :4134    NA's   :4156   NA's   :4135    NA's   :4001   
    ##   FW1MAREND_Y   STOPLIVE_Y_W1    FWPEDUC_W1     FWPMARBF_W1    STRTLIVE_Y_FC1
    ##  Min.   :1995   Min.   :1994   Min.   :1.000   Min.   :1.000   Min.   :1990  
    ##  1st Qu.:2008   1st Qu.:2007   1st Qu.:2.000   1st Qu.:5.000   1st Qu.:2003  
    ##  Median :2013   Median :2012   Median :3.000   Median :5.000   Median :2009  
    ##  Mean   :2173   Mean   :2146   Mean   :3.349   Mean   :4.549   Mean   :2228  
    ##  3rd Qu.:2018   3rd Qu.:2017   3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:2015  
    ##  Max.   :9999   Max.   :9999   Max.   :9.000   Max.   :8.000   Max.   :9999  
    ##  NA's   :4024   NA's   :4014   NA's   :4001    NA's   :4001    NA's   :3644  
    ##    AGELIV_FC1     ENGAGTHN_FC1  STOPLIVE_Y_FC1  FWPEDUC_FC1     FWPMARBF_FC1  
    ##  Min.   :11.00   Min.   :1.00   Min.   :1991   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:19.00   1st Qu.:5.00   1st Qu.:2005   1st Qu.:2.000   1st Qu.:5.000  
    ##  Median :22.00   Median :5.00   Median :2012   Median :3.000   Median :5.000  
    ##  Mean   :24.29   Mean   :4.58   Mean   :2230   Mean   :3.149   Mean   :4.664  
    ##  3rd Qu.:26.00   3rd Qu.:5.00   3rd Qu.:2017   3rd Qu.:5.000   3rd Qu.:5.000  
    ##  Max.   :99.00   Max.   :9.00   Max.   :9999   Max.   :9.000   Max.   :9.000  
    ##  NA's   :3644    NA's   :3644   NA's   :3644   NA's   :3644    NA's   :3644   
    ##     FPPROBE         EVBIOKID       NUMBIOKID         ONEMOM     
    ##  Min.   :1.000   Min.   :1.000   Min.   : 1.00   Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:1.000   1st Qu.: 1.00   1st Qu.:1.000  
    ##  Median :5.000   Median :5.000   Median : 2.00   Median :1.000  
    ##  Mean   :3.433   Mean   :3.296   Mean   : 2.31   Mean   :1.839  
    ##  3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.: 3.00   3rd Qu.:1.000  
    ##  Max.   :9.000   Max.   :9.000   Max.   :98.00   Max.   :5.000  
    ##  NA's   :2206    NA's   :1009    NA's   :2917    NA's   :3436   
    ##      MOMWHO       BCMOMWHO_01     BCMOMAGE_01       BCSEX_01    YRBIOCHILD_01 
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.00   Min.   :1987  
    ##  1st Qu.:1.000   1st Qu.:5.000   1st Qu.:2.000   1st Qu.:1.00   1st Qu.:2008  
    ##  Median :1.000   Median :6.000   Median :3.000   Median :1.00   Median :2013  
    ##  Mean   :2.081   Mean   :5.582   Mean   :2.889   Mean   :1.51   Mean   :2083  
    ##  3rd Qu.:2.000   3rd Qu.:7.000   3rd Qu.:4.000   3rd Qu.:2.00   3rd Qu.:2018  
    ##  Max.   :9.000   Max.   :8.000   Max.   :9.000   Max.   :9.00   Max.   :9999  
    ##  NA's   :3117    NA's   :4175    NA's   :2921    NA's   :2921   NA's   :2921  
    ##     BCAGE_01      BCAGEGRP_01     BCMARLIV_01     BCLRNPRG_01   
    ##  Min.   : 0.00   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.: 5.00   1st Qu.:2.000   1st Qu.:1.000   1st Qu.:1.000  
    ##  Median :10.00   Median :2.000   Median :1.000   Median :1.000  
    ##  Mean   :10.77   Mean   :2.455   Mean   :1.456   Mean   :1.104  
    ##  3rd Qu.:15.00   3rd Qu.:2.000   3rd Qu.:2.000   3rd Qu.:1.000  
    ##  Max.   :99.00   Max.   :8.000   Max.   :9.000   Max.   :8.000  
    ##  NA's   :2933    NA's   :4360    NA's   :3045    NA's   :4112   
    ##   LIVEHERE_01     ALIVENOW_01     BCNOWLIV_01       BCRES_01    
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :0.000  
    ##  1st Qu.:1.000   1st Qu.:1.000   1st Qu.:1.000   1st Qu.:0.000  
    ##  Median :1.000   Median :1.000   Median :1.000   Median :0.000  
    ##  Mean   :2.736   Mean   :1.247   Mean   :1.407   Mean   :0.245  
    ##  3rd Qu.:5.000   3rd Qu.:1.000   3rd Qu.:1.000   3rd Qu.:0.000  
    ##  Max.   :8.000   Max.   :9.000   Max.   :8.000   Max.   :5.000  
    ##  NA's   :3841    NA's   :4144    NA's   :4157    NA's   :3174   
    ##   BCSIGNBC_01      BCCOURT_01     BCGENTST_01     LIVCHEVR_01   
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:5.000   1st Qu.:1.000   1st Qu.:1.000  
    ##  Median :1.000   Median :5.000   Median :5.000   Median :5.000  
    ##  Mean   :1.359   Mean   :4.415   Mean   :3.937   Mean   :3.417  
    ##  3rd Qu.:1.000   3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:5.000  
    ##  Max.   :9.000   Max.   :5.000   Max.   :9.000   Max.   :5.000  
    ##  NA's   :3961    NA's   :3961    NA's   :3961    NA's   :4323   
    ##    BCWANT_01      BCTIMING_01      BCSOONN_01      BCSOONNMY_01  
    ##  Min.   :1.000   Min.   :1.000   Min.   :   1.0   Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:2.000   1st Qu.:   2.0   1st Qu.:2.000  
    ##  Median :1.000   Median :2.000   Median :   4.0   Median :2.000  
    ##  Mean   :1.325   Mean   :1.984   Mean   : 289.6   Mean   :1.771  
    ##  3rd Qu.:1.000   3rd Qu.:2.000   3rd Qu.:   5.5   3rd Qu.:2.000  
    ##  Max.   :9.000   Max.   :4.000   Max.   :9998.0   Max.   :2.000  
    ##  NA's   :3999    NA's   :4124    NA's   :4336     NA's   :4336   
    ##     BCHPY_01       BCMOMWHO_02     BCMOMAGE_02       BCSEX_02    YRBIOCHILD_02 
    ##  Min.   : 0.000   Min.   :1.000   Min.   :1.000   Min.   :1.00   Min.   :1992  
    ##  1st Qu.:10.000   1st Qu.:1.000   1st Qu.:2.000   1st Qu.:1.00   1st Qu.:2010  
    ##  Median :10.000   Median :5.000   Median :3.000   Median :1.00   Median :2015  
    ##  Mean   : 9.253   Mean   :4.383   Mean   :2.903   Mean   :1.52   Mean   :2124  
    ##  3rd Qu.:10.000   3rd Qu.:7.000   3rd Qu.:3.250   3rd Qu.:2.00   3rd Qu.:2019  
    ##  Max.   :10.000   Max.   :9.000   Max.   :9.000   Max.   :9.00   Max.   :9999  
    ##  NA's   :3999     NA's   :4175    NA's   :4175    NA's   :3436   NA's   :3436  
    ##     BCAGE_02       BCAGEGRP_02     MULTBIRT_02     BCMARLIV_02   
    ##  Min.   : 0.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.: 4.000   1st Qu.:1.750   1st Qu.:1.000   1st Qu.:1.000  
    ##  Median : 8.000   Median :2.000   Median :1.000   Median :1.000  
    ##  Mean   : 9.177   Mean   :2.917   Mean   :2.346   Mean   :1.336  
    ##  3rd Qu.:13.000   3rd Qu.:3.000   3rd Qu.:5.000   3rd Qu.:1.000  
    ##  Max.   :99.000   Max.   :8.000   Max.   :8.000   Max.   :8.000  
    ##  NA's   :3447     NA's   :4359    NA's   :4345    NA's   :3522   
    ##   BCLRNPRG_02     LIVEHERE_02     ALIVENOW_02     BCNOWLIV_02   
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:1.000   1st Qu.:1.000   1st Qu.:1.000  
    ##  Median :1.000   Median :1.000   Median :1.000   Median :1.000  
    ##  Mean   :1.079   Mean   :2.683   Mean   :1.324   Mean   :1.494  
    ##  3rd Qu.:1.000   3rd Qu.:5.000   3rd Qu.:1.000   3rd Qu.:1.000  
    ##  Max.   :2.000   Max.   :9.000   Max.   :5.000   Max.   :8.000  
    ##  NA's   :4245    NA's   :4015    NA's   :4223    NA's   :4217   
    ##     BCRES_02      BCSIGNBC_02      BCCOURT_02     BCGENTST_02   
    ##  Min.   :0.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:0.000   1st Qu.:1.000   1st Qu.:5.000   1st Qu.:1.000  
    ##  Median :0.000   Median :1.000   Median :5.000   Median :5.000  
    ##  Mean   :0.233   Mean   :1.582   Mean   :4.461   Mean   :3.978  
    ##  3rd Qu.:0.000   3rd Qu.:1.000   3rd Qu.:5.000   3rd Qu.:5.000  
    ##  Max.   :5.000   Max.   :9.000   Max.   :8.000   Max.   :9.000  
    ##  NA's   :3556    NA's   :4139    NA's   :4139    NA's   :4139   
    ##   LIVCHEVR_02      BCWANT_02      BCTIMING_02      BCSOONN_02    
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :   1.0  
    ##  1st Qu.:2.000   1st Qu.:1.000   1st Qu.:2.000   1st Qu.:   1.0  
    ##  Median :5.000   Median :1.000   Median :2.000   Median :   1.0  
    ##  Mean   :3.933   Mean   :1.475   Mean   :2.079   Mean   : 801.3  
    ##  3rd Qu.:5.000   3rd Qu.:1.000   3rd Qu.:2.000   3rd Qu.:   2.0  
    ##  Max.   :5.000   Max.   :9.000   Max.   :9.000   Max.   :9999.0  
    ##  NA's   :4341    NA's   :4087    NA's   :4182    NA's   :4346    
    ##   BCSOONNMY_02     BCHPY_02      BCMOMWHO_03     BCMOMAGE_03       BCSEX_03    
    ##  Min.   :1.00   Min.   : 0.00   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:2.00   1st Qu.:10.00   1st Qu.:1.000   1st Qu.:2.000   1st Qu.:1.000  
    ##  Median :2.00   Median :10.00   Median :5.000   Median :3.000   Median :2.000  
    ##  Mean   :2.48   Mean   : 9.68   Mean   :3.879   Mean   :3.137   Mean   :1.576  
    ##  3rd Qu.:2.00   3rd Qu.:10.00   3rd Qu.:7.000   3rd Qu.:4.000   3rd Qu.:2.000  
    ##  Max.   :9.00   Max.   :98.00   Max.   :8.000   Max.   :9.000   Max.   :8.000  
    ##  NA's   :4346   NA's   :4087    NA's   :4247    NA's   :4247    NA's   :4003   
    ##  YRBIOCHILD_03     BCAGE_03       BCAGEGRP_03    MULTBIRT_03     BCMARLIV_03   
    ##  Min.   :1994   Min.   : 0.000   Min.   :1.0    Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:2010   1st Qu.: 3.000   1st Qu.:1.0    1st Qu.:1.000   1st Qu.:1.000  
    ##  Median :2015   Median : 7.000   Median :1.5    Median :1.000   Median :1.000  
    ##  Mean   :2166   Mean   : 8.953   Mean   :2.5    Mean   :2.765   Mean   :1.411  
    ##  3rd Qu.:2019   3rd Qu.:12.000   3rd Qu.:2.0    3rd Qu.:5.000   3rd Qu.:2.000  
    ##  Max.   :9998   Max.   :99.000   Max.   :8.0    Max.   :8.000   Max.   :8.000  
    ##  NA's   :4003   NA's   :4009     NA's   :4365   NA's   :4354    NA's   :4035   
    ##   BCLRNPRG_03     LIVEHERE_03     ALIVENOW_03    BCNOWLIV_03       BCRES_03    
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.0    Min.   :1.000   Min.   :0.000  
    ##  1st Qu.:1.000   1st Qu.:1.000   1st Qu.:1.0    1st Qu.:1.000   1st Qu.:0.000  
    ##  Median :1.000   Median :1.000   Median :1.0    Median :1.000   Median :0.000  
    ##  Mean   :1.222   Mean   :2.548   Mean   :1.2    Mean   :1.559   Mean   :0.243  
    ##  3rd Qu.:1.000   3rd Qu.:5.000   3rd Qu.:1.0    3rd Qu.:1.000   3rd Qu.:0.000  
    ##  Max.   :2.000   Max.   :8.000   Max.   :5.0    Max.   :8.000   Max.   :5.000  
    ##  NA's   :4326    NA's   :4214    NA's   :4311   NA's   :4303    NA's   :4042   
    ##   BCSIGNBC_03      BCCOURT_03     BCGENTST_03     LIVCHEVR_03     BCWANT_03    
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.0    Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:5.000   1st Qu.:5.000   1st Qu.:5.0    1st Qu.:1.000  
    ##  Median :1.000   Median :5.000   Median :5.000   Median :5.0    Median :1.000  
    ##  Mean   :1.835   Mean   :4.633   Mean   :4.183   Mean   :4.6    Mean   :1.873  
    ##  3rd Qu.:1.000   3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:5.0    3rd Qu.:2.000  
    ##  Max.   :8.000   Max.   :5.000   Max.   :8.000   Max.   :5.0    Max.   :9.000  
    ##  NA's   :4262    NA's   :4262    NA's   :4262    NA's   :4361   NA's   :4245   
    ##   BCTIMING_03      BCSOONN_03      BCSOONNMY_03     BCHPY_03     
    ##  Min.   :1.000   Min.   :   1.0   Min.   :1.0    Min.   : 0.000  
    ##  1st Qu.:2.000   1st Qu.:   1.0   1st Qu.:2.0    1st Qu.: 9.000  
    ##  Median :2.000   Median :   3.0   Median :2.0    Median :10.000  
    ##  Mean   :1.988   Mean   :2001.8   Mean   :2.6    Mean   : 9.063  
    ##  3rd Qu.:2.000   3rd Qu.:   5.5   3rd Qu.:2.0    3rd Qu.:10.000  
    ##  Max.   :4.000   Max.   :9999.0   Max.   :9.0    Max.   :10.000  
    ##  NA's   :4291    NA's   :4361     NA's   :4361   NA's   :4245    
    ##   BCMOMWHO_04     BCMOMAGE_04       BCSEX_04    YRBIOCHILD_04     BCAGE_04     
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.00   Min.   :1998   Min.   : 0.000  
    ##  1st Qu.:1.000   1st Qu.:2.000   1st Qu.:1.00   1st Qu.:2010   1st Qu.: 2.000  
    ##  Median :2.000   Median :3.000   Median :1.00   Median :2017   Median : 5.000  
    ##  Mean   :3.508   Mean   :3.143   Mean   :1.59   Mean   :2015   Mean   : 7.955  
    ##  3rd Qu.:7.000   3rd Qu.:4.000   3rd Qu.:2.00   3rd Qu.:2020   3rd Qu.:12.000  
    ##  Max.   :7.000   Max.   :9.000   Max.   :9.00   Max.   :2023   Max.   :99.000  
    ##  NA's   :4308    NA's   :4308    NA's   :4237   NA's   :4237   NA's   :4237    
    ##  BCAGEGRP_04     MULTBIRT_04    BCMARLIV_04    BCLRNPRG_04     LIVEHERE_04   
    ##  Mode:logical   Min.   :1      Min.   :1.00   Min.   :1.000   Min.   :1.000  
    ##  NA's:4371      1st Qu.:1      1st Qu.:1.00   1st Qu.:1.000   1st Qu.:1.000  
    ##                 Median :1      Median :1.00   Median :1.000   Median :1.000  
    ##                 Mean   :1      Mean   :1.56   Mean   :1.217   Mean   :2.254  
    ##                 3rd Qu.:1      3rd Qu.:2.00   3rd Qu.:1.000   3rd Qu.:5.000  
    ##                 Max.   :1      Max.   :3.00   Max.   :2.000   Max.   :5.000  
    ##                 NA's   :4369   NA's   :4246   NA's   :4348    NA's   :4304   
    ##   ALIVENOW_04     BCNOWLIV_04       BCRES_04      BCSIGNBC_04   
    ##  Min.   :1.000   Min.   :1.000   Min.   :0.000   Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:1.000   1st Qu.:0.000   1st Qu.:1.000  
    ##  Median :1.000   Median :1.000   Median :0.000   Median :1.000  
    ##  Mean   :1.571   Mean   :1.286   Mean   :0.203   Mean   :2.071  
    ##  3rd Qu.:1.000   3rd Qu.:1.000   3rd Qu.:0.000   3rd Qu.:5.000  
    ##  Max.   :9.000   Max.   :5.000   Max.   :5.000   Max.   :5.000  
    ##  NA's   :4350    NA's   :4350    NA's   :4248    NA's   :4315   
    ##    BCCOURT_04     BCGENTST_04     LIVCHEVR_04     BCWANT_04     BCTIMING_04   
    ##  Min.   :1.000   Min.   :1.000   Min.   :5      Min.   :1.00   Min.   :1.000  
    ##  1st Qu.:5.000   1st Qu.:1.000   1st Qu.:5      1st Qu.:1.00   1st Qu.:2.000  
    ##  Median :5.000   Median :5.000   Median :5      Median :1.00   Median :2.000  
    ##  Mean   :4.286   Mean   :3.571   Mean   :5      Mean   :1.82   Mean   :1.938  
    ##  3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:5      3rd Qu.:3.00   3rd Qu.:2.000  
    ##  Max.   :5.000   Max.   :5.000   Max.   :5      Max.   :4.00   Max.   :3.000  
    ##  NA's   :4315    NA's   :4315    NA's   :4365   NA's   :4310   NA's   :4339   
    ##    BCSOONN_04    BCSOONNMY_04     BCHPY_04       BCMOMWHO_05     BCMOMAGE_05   
    ##  Min.   : 1.0   Min.   :1.0    Min.   : 0.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.: 2.0   1st Qu.:1.0    1st Qu.: 8.000   1st Qu.:1.000   1st Qu.:2.000  
    ##  Median : 2.0   Median :2.0    Median :10.000   Median :4.000   Median :3.000  
    ##  Mean   : 4.6   Mean   :1.6    Mean   : 8.721   Mean   :3.613   Mean   :3.194  
    ##  3rd Qu.: 6.0   3rd Qu.:2.0    3rd Qu.:10.000   3rd Qu.:5.500   3rd Qu.:4.000  
    ##  Max.   :12.0   Max.   :2.0    Max.   :10.000   Max.   :7.000   Max.   :9.000  
    ##  NA's   :4366   NA's   :4366   NA's   :4310     NA's   :4340    NA's   :4340   
    ##     BCSEX_05     YRBIOCHILD_05     BCAGE_05      BCAGEGRP_05     MULTBIRT_05  
    ##  Min.   :1.000   Min.   :2002   Min.   : 0.000   Mode:logical   Min.   :1     
    ##  1st Qu.:1.000   1st Qu.:2010   1st Qu.: 3.000   NA's:4371      1st Qu.:1     
    ##  Median :1.000   Median :2015   Median : 8.000                  Median :1     
    ##  Mean   :1.562   Mean   :2014   Mean   : 9.833                  Mean   :1     
    ##  3rd Qu.:2.000   3rd Qu.:2020   3rd Qu.:13.000                  3rd Qu.:1     
    ##  Max.   :9.000   Max.   :2023   Max.   :99.000                  Max.   :1     
    ##  NA's   :4323    NA's   :4323   NA's   :4323                    NA's   :4367  
    ##   BCMARLIV_05     BCLRNPRG_05     LIVEHERE_05     ALIVENOW_05    BCNOWLIV_05   
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1      Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:1.000   1st Qu.:1.000   1st Qu.:1      1st Qu.:1.000  
    ##  Median :1.000   Median :1.000   Median :1.000   Median :1      Median :1.000  
    ##  Mean   :1.619   Mean   :1.273   Mean   :2.692   Mean   :1      Mean   :1.667  
    ##  3rd Qu.:2.000   3rd Qu.:1.500   3rd Qu.:5.000   3rd Qu.:1      3rd Qu.:2.000  
    ##  Max.   :3.000   Max.   :2.000   Max.   :5.000   Max.   :1      Max.   :5.000  
    ##  NA's   :4329    NA's   :4360    NA's   :4345    NA's   :4360   NA's   :4356   
    ##     BCRES_05      BCSIGNBC_05      BCCOURT_05     BCGENTST_05     LIVCHEVR_05  
    ##  Min.   :0.000   Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1     
    ##  1st Qu.:0.000   1st Qu.:1.000   1st Qu.:5.000   1st Qu.:5.000   1st Qu.:1     
    ##  Median :0.000   Median :1.000   Median :5.000   Median :5.000   Median :3     
    ##  Mean   :0.467   Mean   :2.818   Mean   :4.636   Mean   :4.091   Mean   :3     
    ##  3rd Qu.:0.000   3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:5     
    ##  Max.   :5.000   Max.   :5.000   Max.   :5.000   Max.   :5.000   Max.   :5     
    ##  NA's   :4326    NA's   :4349    NA's   :4349    NA's   :4349    NA's   :4367  
    ##    BCWANT_05      BCTIMING_05     BCSOONN_05    BCSOONNMY_05     BCHPY_05     
    ##  Min.   :1.000   Min.   :1.00   Min.   :2.0    Min.   :2      Min.   : 2.000  
    ##  1st Qu.:1.000   1st Qu.:1.75   1st Qu.:2.5    1st Qu.:2      1st Qu.: 9.000  
    ##  Median :2.000   Median :2.00   Median :3.0    Median :2      Median :10.000  
    ##  Mean   :2.133   Mean   :2.00   Mean   :3.0    Mean   :2      Mean   : 8.867  
    ##  3rd Qu.:3.000   3rd Qu.:2.00   3rd Qu.:3.5    3rd Qu.:2      3rd Qu.:10.000  
    ##  Max.   :4.000   Max.   :4.00   Max.   :4.0    Max.   :2      Max.   :10.000  
    ##  NA's   :4356    NA's   :4363   NA's   :4369   NA's   :4369   NA's   :4356    
    ##   BCMOMWHO_06     BCMOMAGE_06       BCSEX_06     YRBIOCHILD_06 
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :2009  
    ##  1st Qu.:1.000   1st Qu.:2.000   1st Qu.:1.000   1st Qu.:2012  
    ##  Median :2.000   Median :3.000   Median :2.000   Median :2016  
    ##  Mean   :2.786   Mean   :2.857   Mean   :1.611   Mean   :2015  
    ##  3rd Qu.:4.500   3rd Qu.:4.000   3rd Qu.:2.000   3rd Qu.:2018  
    ##  Max.   :7.000   Max.   :4.000   Max.   :2.000   Max.   :2023  
    ##  NA's   :4357    NA's   :4357    NA's   :4353    NA's   :4353  
    ##     BCAGE_06      BCAGEGRP_06    MULTBIRT_06     BCMARLIV_06     BCLRNPRG_06  
    ##  Min.   : 0.000   Mode:logical   Mode:logical   Min.   :1.000   Min.   :1.00  
    ##  1st Qu.: 4.250   NA's:4371      NA's:4371      1st Qu.:1.000   1st Qu.:1.00  
    ##  Median : 6.500                                 Median :2.000   Median :1.00  
    ##  Mean   : 6.889                                 Mean   :1.706   Mean   :1.25  
    ##  3rd Qu.:10.000                                 3rd Qu.:2.000   3rd Qu.:1.25  
    ##  Max.   :14.000                                 Max.   :3.000   Max.   :2.00  
    ##  NA's   :4353                                   NA's   :4354    NA's   :4367  
    ##   LIVEHERE_06     ALIVENOW_06    BCNOWLIV_06      BCRES_06      BCSIGNBC_06  
    ##  Min.   :1.000   Min.   :1.0    Min.   :1      Min.   :0.000   Min.   :1.0   
    ##  1st Qu.:1.000   1st Qu.:1.0    1st Qu.:1      1st Qu.:0.000   1st Qu.:1.0   
    ##  Median :1.000   Median :5.0    Median :1      Median :0.000   Median :1.0   
    ##  Mean   :2.538   Mean   :3.4    Mean   :1      Mean   :0.133   Mean   :2.5   
    ##  3rd Qu.:5.000   3rd Qu.:5.0    3rd Qu.:1      3rd Qu.:0.000   3rd Qu.:5.0   
    ##  Max.   :5.000   Max.   :5.0    Max.   :1      Max.   :1.000   Max.   :5.0   
    ##  NA's   :4358    NA's   :4366   NA's   :4369   NA's   :4356    NA's   :4363  
    ##    BCCOURT_06    BCGENTST_06    LIVCHEVR_06     BCWANT_06     BCTIMING_06  
    ##  Min.   :1.0    Min.   :1.0    Min.   :1      Min.   :1.0    Min.   :1.00  
    ##  1st Qu.:5.0    1st Qu.:5.0    1st Qu.:1      1st Qu.:1.0    1st Qu.:1.25  
    ##  Median :5.0    Median :5.0    Median :1      Median :2.0    Median :1.50  
    ##  Mean   :4.5    Mean   :4.5    Mean   :1      Mean   :2.2    Mean   :1.50  
    ##  3rd Qu.:5.0    3rd Qu.:5.0    3rd Qu.:1      3rd Qu.:3.0    3rd Qu.:1.75  
    ##  Max.   :5.0    Max.   :5.0    Max.   :1      Max.   :4.0    Max.   :2.00  
    ##  NA's   :4363   NA's   :4363   NA's   :4370   NA's   :4366   NA's   :4369  
    ##    BCSOONN_06    BCSOONNMY_06     BCHPY_06     BCMOMWHO_07    BCMOMAGE_07  
    ##  Min.   :2      Min.   :2      Min.   : 6     Min.   :1.0    Min.   :2.0   
    ##  1st Qu.:2      1st Qu.:2      1st Qu.: 9     1st Qu.:1.0    1st Qu.:3.0   
    ##  Median :2      Median :2      Median :10     Median :1.0    Median :4.0   
    ##  Mean   :2      Mean   :2      Mean   : 9     Mean   :2.4    Mean   :3.4   
    ##  3rd Qu.:2      3rd Qu.:2      3rd Qu.:10     3rd Qu.:2.0    3rd Qu.:4.0   
    ##  Max.   :2      Max.   :2      Max.   :10     Max.   :7.0    Max.   :4.0   
    ##  NA's   :4370   NA's   :4370   NA's   :4366   NA's   :4366   NA's   :4366  
    ##     BCSEX_07     YRBIOCHILD_07     BCAGE_07      BCAGEGRP_07    MULTBIRT_07   
    ##  Min.   :1.000   Min.   :2008   Min.   : 0.000   Mode:logical   Mode:logical  
    ##  1st Qu.:1.000   1st Qu.:2013   1st Qu.: 2.000   NA's:4371      NA's:4371     
    ##  Median :2.000   Median :2017   Median : 4.000                                
    ##  Mean   :1.571   Mean   :2016   Mean   : 5.857                                
    ##  3rd Qu.:2.000   3rd Qu.:2020   3rd Qu.: 9.000                                
    ##  Max.   :2.000   Max.   :2022   Max.   :15.000                                
    ##  NA's   :4364    NA's   :4364   NA's   :4364                                  
    ##   BCMARLIV_07     BCLRNPRG_07    LIVEHERE_07     ALIVENOW_07    BCNOWLIV_07  
    ##  Min.   :1.000   Min.   :2      Min.   :1.000   Min.   :1      Min.   :1     
    ##  1st Qu.:1.500   1st Qu.:2      1st Qu.:1.000   1st Qu.:1      1st Qu.:1     
    ##  Median :2.000   Median :2      Median :1.000   Median :1      Median :1     
    ##  Mean   :1.857   Mean   :2      Mean   :1.667   Mean   :1      Mean   :1     
    ##  3rd Qu.:2.000   3rd Qu.:2      3rd Qu.:1.000   3rd Qu.:1      3rd Qu.:1     
    ##  Max.   :3.000   Max.   :2      Max.   :5.000   Max.   :1      Max.   :1     
    ##  NA's   :4364    NA's   :4370   NA's   :4365    NA's   :4370   NA's   :4370  
    ##     BCRES_07      BCSIGNBC_07     BCCOURT_07    BCGENTST_07    LIVCHEVR_07  
    ##  Min.   :0.000   Min.   :1.0    Min.   :5      Min.   :1.0    Min.   :5     
    ##  1st Qu.:0.000   1st Qu.:1.0    1st Qu.:5      1st Qu.:5.0    1st Qu.:5     
    ##  Median :0.000   Median :1.0    Median :5      Median :5.0    Median :5     
    ##  Mean   :0.143   Mean   :2.6    Mean   :5      Mean   :4.2    Mean   :5     
    ##  3rd Qu.:0.000   3rd Qu.:5.0    3rd Qu.:5      3rd Qu.:5.0    3rd Qu.:5     
    ##  Max.   :1.000   Max.   :5.0    Max.   :5      Max.   :5.0    Max.   :5     
    ##  NA's   :4364    NA's   :4366   NA's   :4366   NA's   :4366   NA's   :4370  
    ##    BCWANT_07     BCTIMING_07   BCSOONN_07     BCSOONNMY_07      BCHPY_07   
    ##  Min.   :1.0    Min.   :2.00   Mode:logical   Mode:logical   Min.   : 2    
    ##  1st Qu.:1.0    1st Qu.:2.25   NA's:4371      NA's:4371      1st Qu.: 8    
    ##  Median :1.0    Median :2.50                                 Median :10    
    ##  Mean   :1.5    Mean   :2.50                                 Mean   : 8    
    ##  3rd Qu.:1.5    3rd Qu.:2.75                                 3rd Qu.:10    
    ##  Max.   :3.0    Max.   :3.00                                 Max.   :10    
    ##  NA's   :4367   NA's   :4369                                 NA's   :4367  
    ##   BCMOMWHO_08    BCMOMAGE_08      BCSEX_08     YRBIOCHILD_08     BCAGE_08     
    ##  Min.   :1.0    Min.   :3.00   Min.   :1.000   Min.   :2011   Min.   : 2.000  
    ##  1st Qu.:2.5    1st Qu.:3.25   1st Qu.:1.000   1st Qu.:2013   1st Qu.: 4.000  
    ##  Median :4.0    Median :3.50   Median :1.000   Median :2015   Median : 6.000  
    ##  Mean   :4.0    Mean   :3.50   Mean   :1.333   Mean   :2015   Mean   : 6.667  
    ##  3rd Qu.:5.5    3rd Qu.:3.75   3rd Qu.:1.500   3rd Qu.:2017   3rd Qu.: 9.000  
    ##  Max.   :7.0    Max.   :4.00   Max.   :2.000   Max.   :2019   Max.   :12.000  
    ##  NA's   :4369   NA's   :4369   NA's   :4368    NA's   :4368   NA's   :4368    
    ##  BCAGEGRP_08    MULTBIRT_08     BCMARLIV_08    BCLRNPRG_08    LIVEHERE_08  
    ##  Mode:logical   Mode:logical   Min.   :1.0    Min.   :1      Min.   :1     
    ##  NA's:4371      NA's:4371      1st Qu.:1.5    1st Qu.:1      1st Qu.:2     
    ##                                Median :2.0    Median :1      Median :3     
    ##                                Mean   :2.0    Mean   :1      Mean   :3     
    ##                                3rd Qu.:2.5    3rd Qu.:1      3rd Qu.:4     
    ##                                Max.   :3.0    Max.   :1      Max.   :5     
    ##                                NA's   :4368   NA's   :4370   NA's   :4369  
    ##   ALIVENOW_08    BCNOWLIV_08      BCRES_08      BCSIGNBC_08     BCCOURT_08  
    ##  Min.   :1      Min.   :1      Min.   :0.000   Min.   :1      Min.   :5     
    ##  1st Qu.:1      1st Qu.:1      1st Qu.:0.000   1st Qu.:2      1st Qu.:5     
    ##  Median :1      Median :1      Median :0.000   Median :3      Median :5     
    ##  Mean   :1      Mean   :1      Mean   :0.333   Mean   :3      Mean   :5     
    ##  3rd Qu.:1      3rd Qu.:1      3rd Qu.:0.500   3rd Qu.:4      3rd Qu.:5     
    ##  Max.   :1      Max.   :1      Max.   :1.000   Max.   :5      Max.   :5     
    ##  NA's   :4370   NA's   :4370   NA's   :4368    NA's   :4369   NA's   :4369  
    ##   BCGENTST_08    LIVCHEVR_08     BCWANT_08    BCTIMING_08    BCSOONN_08    
    ##  Min.   :5      Min.   :5      Min.   :2      Mode:logical   Mode:logical  
    ##  1st Qu.:5      1st Qu.:5      1st Qu.:2      NA's:4371      NA's:4371     
    ##  Median :5      Median :5      Median :2                                   
    ##  Mean   :5      Mean   :5      Mean   :2                                   
    ##  3rd Qu.:5      3rd Qu.:5      3rd Qu.:2                                   
    ##  Max.   :5      Max.   :5      Max.   :2                                   
    ##  NA's   :4369   NA's   :4370   NA's   :4370                                
    ##  BCSOONNMY_08      BCHPY_08     BCMOMWHO_09    BCMOMAGE_09      BCSEX_09   
    ##  Mode:logical   Min.   :10     Min.   :1      Min.   :3      Min.   :1.00  
    ##  NA's:4371      1st Qu.:10     1st Qu.:1      1st Qu.:3      1st Qu.:1.25  
    ##                 Median :10     Median :1      Median :3      Median :1.50  
    ##                 Mean   :10     Mean   :1      Mean   :3      Mean   :1.50  
    ##                 3rd Qu.:10     3rd Qu.:1      3rd Qu.:3      3rd Qu.:1.75  
    ##                 Max.   :10     Max.   :1      Max.   :3      Max.   :2.00  
    ##                 NA's   :4370   NA's   :4370   NA's   :4370   NA's   :4369  
    ##  YRBIOCHILD_09     BCAGE_09    BCAGEGRP_09    MULTBIRT_09     BCMARLIV_09  
    ##  Min.   :2015   Min.   :0      Mode:logical   Mode:logical   Min.   :1.00  
    ##  1st Qu.:2017   1st Qu.:2      NA's:4371      NA's:4371      1st Qu.:1.25  
    ##  Median :2018   Median :4                                    Median :1.50  
    ##  Mean   :2018   Mean   :4                                    Mean   :1.50  
    ##  3rd Qu.:2020   3rd Qu.:6                                    3rd Qu.:1.75  
    ##  Max.   :2022   Max.   :8                                    Max.   :2.00  
    ##  NA's   :4369   NA's   :4369                                 NA's   :4369  
    ##  BCLRNPRG_09     LIVEHERE_09   ALIVENOW_09    BCNOWLIV_09       BCRES_09   
    ##  Mode:logical   Min.   :1      Mode:logical   Mode:logical   Min.   :0     
    ##  NA's:4371      1st Qu.:1      NA's:4371      NA's:4371      1st Qu.:0     
    ##                 Median :1                                    Median :0     
    ##                 Mean   :1                                    Mean   :0     
    ##                 3rd Qu.:1                                    3rd Qu.:0     
    ##                 Max.   :1                                    Max.   :0     
    ##                 NA's   :4369                                 NA's   :4369  
    ##   BCSIGNBC_09     BCCOURT_09    BCGENTST_09   LIVCHEVR_09      BCWANT_09   
    ##  Min.   :1      Min.   :5      Min.   :5      Mode:logical   Min.   :1     
    ##  1st Qu.:1      1st Qu.:5      1st Qu.:5      NA's:4371      1st Qu.:1     
    ##  Median :1      Median :5      Median :5                     Median :1     
    ##  Mean   :1      Mean   :5      Mean   :5                     Mean   :1     
    ##  3rd Qu.:1      3rd Qu.:5      3rd Qu.:5                     3rd Qu.:1     
    ##  Max.   :1      Max.   :5      Max.   :5                     Max.   :1     
    ##  NA's   :4370   NA's   :4370   NA's   :4370                  NA's   :4370  
    ##  BCTIMING_09       BCHPY_09    BCSOONN_09     BCSOONNMY_09    BCMOMWHO_10  
    ##  Mode:logical   Min.   :10     Mode:logical   Mode:logical   Min.   :1     
    ##  NA's:4371      1st Qu.:10     NA's:4371      NA's:4371      1st Qu.:1     
    ##                 Median :10                                   Median :1     
    ##                 Mean   :10                                   Mean   :1     
    ##                 3rd Qu.:10                                   3rd Qu.:1     
    ##                 Max.   :10                                   Max.   :1     
    ##                 NA's   :4370                                 NA's   :4370  
    ##   BCMOMAGE_10      BCSEX_10    YRBIOCHILD_10     BCAGE_10    BCAGEGRP_10   
    ##  Min.   :3      Min.   :1.00   Min.   :2017   Min.   :0.0    Mode:logical  
    ##  1st Qu.:3      1st Qu.:1.25   1st Qu.:2018   1st Qu.:1.5    NA's:4371     
    ##  Median :3      Median :1.50   Median :2020   Median :3.0                  
    ##  Mean   :3      Mean   :1.50   Mean   :2020   Mean   :3.0                  
    ##  3rd Qu.:3      3rd Qu.:1.75   3rd Qu.:2021   3rd Qu.:4.5                  
    ##  Max.   :3      Max.   :2.00   Max.   :2022   Max.   :6.0                  
    ##  NA's   :4370   NA's   :4369   NA's   :4369   NA's   :4369                 
    ##   MULTBIRT_10    BCMARLIV_10   BCLRNPRG_10     LIVEHERE_10   ALIVENOW_10   
    ##  Min.   :1      Min.   :2      Mode:logical   Min.   :1      Mode:logical  
    ##  1st Qu.:1      1st Qu.:2      NA's:4371      1st Qu.:1      NA's:4371     
    ##  Median :1      Median :2                     Median :1                    
    ##  Mean   :1      Mean   :2                     Mean   :1                    
    ##  3rd Qu.:1      3rd Qu.:2                     3rd Qu.:1                    
    ##  Max.   :1      Max.   :2                     Max.   :1                    
    ##  NA's   :4370   NA's   :4370                  NA's   :4370                 
    ##   BCNOWLIV_10      BCRES_10     BCSIGNBC_10     BCCOURT_10    BCGENTST_10  
    ##  Min.   :1      Min.   :0      Min.   :1      Min.   :5      Min.   :5     
    ##  1st Qu.:1      1st Qu.:0      1st Qu.:1      1st Qu.:5      1st Qu.:5     
    ##  Median :1      Median :0      Median :1      Median :5      Median :5     
    ##  Mean   :1      Mean   :0      Mean   :1      Mean   :5      Mean   :5     
    ##  3rd Qu.:1      3rd Qu.:0      3rd Qu.:1      3rd Qu.:5      3rd Qu.:5     
    ##  Max.   :1      Max.   :0      Max.   :1      Max.   :5      Max.   :5     
    ##  NA's   :4370   NA's   :4369   NA's   :4369   NA's   :4369   NA's   :4369  
    ##  LIVCHEVR_10    BCWANT_10      BCTIMING_10    BCSOONN_10     BCSOONNMY_10  
    ##  Mode:logical   Mode:logical   Mode:logical   Mode:logical   Mode:logical  
    ##  NA's:4371      NA's:4371      NA's:4371      NA's:4371      NA's:4371     
    ##                                                                            
    ##                                                                            
    ##                                                                            
    ##                                                                            
    ##                                                                            
    ##  BCHPY_10          CWPKIDS          NBPARENT       NBKDLEGSTAT   
    ##  Mode:logical   Min.   :0.0000   Min.   : 0.000   Min.   :1.000  
    ##  NA's:4371      1st Qu.:0.0000   1st Qu.: 0.000   1st Qu.:5.000  
    ##                 Median :0.0000   Median : 1.000   Median :5.000  
    ##                 Mean   :0.2257   Mean   : 2.741   Mean   :4.111  
    ##                 3rd Qu.:0.0000   3rd Qu.: 1.000   3rd Qu.:5.000  
    ##                 Max.   :1.0000   Max.   :99.000   Max.   :9.000  
    ##                 NA's   :2        NA's   :4209     NA's   :4263   
    ##     NBKADOP1        NBKADOP2        NBKGUARD       EVERADOPT    
    ##  Min.   :1.000   Min.   :0.000   Min.   :0.000   Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:0.000   1st Qu.:0.000   1st Qu.:5.000  
    ##  Median :1.000   Median :0.000   Median :1.000   Median :5.000  
    ##  Mean   :2.111   Mean   :0.429   Mean   :0.857   Mean   :5.001  
    ##  3rd Qu.:4.000   3rd Qu.:0.500   3rd Qu.:1.500   3rd Qu.:5.000  
    ##  Max.   :5.000   Max.   :2.000   Max.   :2.000   Max.   :9.000  
    ##  NA's   :4353    NA's   :4364    NA's   :4364    NA's   :449    
    ##      OTPREG         OTPRGPRB         OTPRGN         OTPREGS       
    ##  Min.   :1.000   Min.   :1.000   Min.   : 1.00   Min.   : 0.0000  
    ##  1st Qu.:5.000   1st Qu.:5.000   1st Qu.: 1.00   1st Qu.: 0.0000  
    ##  Median :5.000   Median :5.000   Median : 1.00   Median : 0.0000  
    ##  Mean   :4.274   Mean   :4.679   Mean   : 1.71   Mean   : 0.2509  
    ##  3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.: 2.00   3rd Qu.: 0.0000  
    ##  Max.   :9.000   Max.   :9.000   Max.   :98.00   Max.   :98.0000  
    ##  NA's   :1009    NA's   :1650    NA's   :3730    NA's   :2        
    ##     PREGSNOW          PREGCHK        TOTPREGS_R     TOTPREGS_CON   
    ##  Min.   :0.00000   Min.   :1.000   Min.   : 0.00   Min.   : 0.000  
    ##  1st Qu.:0.00000   1st Qu.:1.000   1st Qu.: 0.00   1st Qu.: 0.000  
    ##  Median :0.00000   Median :1.000   Median : 1.00   Median : 0.000  
    ##  Mean   :0.02105   Mean   :1.307   Mean   :16.44   Mean   : 1.989  
    ##  3rd Qu.:0.00000   3rd Qu.:1.000   3rd Qu.: 3.00   3rd Qu.: 2.000  
    ##  Max.   :3.00000   Max.   :9.000   Max.   :99.00   Max.   :99.000  
    ##                    NA's   :80      NA's   :4086    NA's   :79      
    ##     ANYKIDS          CRALL           CRALLU5         CRALL518     
    ##  Min.   :1.000   Min.   :0.0000   Min.   :0.000   Min.   :0.0000  
    ##  1st Qu.:1.000   1st Qu.:0.0000   1st Qu.:0.000   1st Qu.:0.0000  
    ##  Median :5.000   Median :0.0000   Median :0.000   Median :0.0000  
    ##  Mean   :3.658   Mean   :0.6544   Mean   :0.221   Mean   :0.4251  
    ##  3rd Qu.:5.000   3rd Qu.:1.0000   3rd Qu.:0.000   3rd Qu.:1.0000  
    ##  Max.   :5.000   Max.   :4.0000   Max.   :2.000   Max.   :3.0000  
    ##  NA's   :2       NA's   :986      NA's   :986     NA's   :986     
    ##     CRMALU5          CRMAL518         CRFEMU5          CRFEM518     
    ##  Min.   :0.0000   Min.   :0.0000   Min.   :0.0000   Min.   :0.0000  
    ##  1st Qu.:0.0000   1st Qu.:0.0000   1st Qu.:0.0000   1st Qu.:0.0000  
    ##  Median :0.0000   Median :0.0000   Median :0.0000   Median :0.0000  
    ##  Mean   :0.1146   Mean   :0.2133   Mean   :0.1102   Mean   :0.2047  
    ##  3rd Qu.:0.0000   3rd Qu.:0.0000   3rd Qu.:0.0000   3rd Qu.:0.0000  
    ##  Max.   :2.0000   Max.   :2.0000   Max.   :2.0000   Max.   :2.0000  
    ##  NA's   :986      NA's   :986      NA's   :986      NA's   :986     
    ##      NCALL           NCALLU5          NCALL518         NCMALU5      
    ##  Min.   :0.0000   Min.   :0.0000   Min.   :0.0000   Min.   :0.0000  
    ##  1st Qu.:0.0000   1st Qu.:0.0000   1st Qu.:0.0000   1st Qu.:0.0000  
    ##  Median :0.0000   Median :0.0000   Median :0.0000   Median :0.0000  
    ##  Mean   :0.1282   Mean   :0.0183   Mean   :0.1099   Mean   :0.0077  
    ##  3rd Qu.:0.0000   3rd Qu.:0.0000   3rd Qu.:0.0000   3rd Qu.:0.0000  
    ##  Max.   :6.0000   Max.   :2.0000   Max.   :5.0000   Max.   :2.0000  
    ##  NA's   :986      NA's   :986      NA's   :986      NA's   :986     
    ##     NCMAL518         NCFEMU5          NCFEM518         RFAGE       
    ##  Min.   :0.0000   Min.   :0.0000   Min.   :0.000   Min.   : 0.000  
    ##  1st Qu.:0.0000   1st Qu.:0.0000   1st Qu.:0.000   1st Qu.: 2.000  
    ##  Median :0.0000   Median :0.0000   Median :0.000   Median : 4.000  
    ##  Mean   :0.0576   Mean   :0.0106   Mean   :0.052   Mean   : 5.551  
    ##  3rd Qu.:0.0000   3rd Qu.:0.0000   3rd Qu.:0.000   3rd Qu.: 9.000  
    ##  Max.   :4.0000   Max.   :2.0000   Max.   :4.000   Max.   :99.000  
    ##  NA's   :986      NA's   :986      NA's   :986     NA's   :3203    
    ##      RFSEX           ROUTG04         RMEAL04        RERRAND04    
    ##  Min.   : 1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.: 1.000   1st Qu.:3.000   1st Qu.:4.000   1st Qu.:3.000  
    ##  Median : 1.000   Median :4.000   Median :5.000   Median :4.000  
    ##  Mean   : 1.907   Mean   :3.572   Mean   :4.579   Mean   :3.471  
    ##  3rd Qu.: 2.000   3rd Qu.:4.000   3rd Qu.:5.000   3rd Qu.:4.000  
    ##  Max.   :99.000   Max.   :5.000   Max.   :5.000   Max.   :5.000  
    ##  NA's   :3194     NA's   :3777    NA's   :3777    NA's   :3777   
    ##     RPLAY04         RREAD04        RAFFECT04       RPRAISE04    
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:4.000   1st Qu.:3.000   1st Qu.:5.000   1st Qu.:5.000  
    ##  Median :5.000   Median :4.000   Median :5.000   Median :5.000  
    ##  Mean   :4.588   Mean   :3.761   Mean   :4.897   Mean   :4.758  
    ##  3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:5.000  
    ##  Max.   :5.000   Max.   :5.000   Max.   :5.000   Max.   :8.000  
    ##  NA's   :3777    NA's   :3777    NA's   :3777    NA's   :3777   
    ##     RFEED04         RBATH04        RDIAPER04         RBED04     
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:4.000   1st Qu.:3.000   1st Qu.:4.000   1st Qu.:4.000  
    ##  Median :5.000   Median :4.000   Median :5.000   Median :5.000  
    ##  Mean   :4.561   Mean   :3.625   Mean   :4.328   Mean   :4.221  
    ##  3rd Qu.:5.000   3rd Qu.:4.000   3rd Qu.:5.000   3rd Qu.:5.000  
    ##  Max.   :5.000   Max.   :5.000   Max.   :5.000   Max.   :8.000  
    ##  NA's   :3777    NA's   :3777    NA's   :3777    NA's   :3777   
    ##     RAPPT04         RDISC04         ROUTG518        RMEAL518    
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:1.000   1st Qu.:3.000   1st Qu.:4.000  
    ##  Median :2.000   Median :2.000   Median :4.000   Median :5.000  
    ##  Mean   :2.177   Mean   :2.158   Mean   :3.429   Mean   :4.387  
    ##  3rd Qu.:2.000   3rd Qu.:3.000   3rd Qu.:4.000   3rd Qu.:5.000  
    ##  Max.   :9.000   Max.   :8.000   Max.   :5.000   Max.   :5.000  
    ##  NA's   :3777    NA's   :3777    NA's   :3790    NA's   :3790   
    ##    RERRAND518      RAFFECT518      RPRAISE518       RTAKE518    
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:3.000   1st Qu.:4.000   1st Qu.:4.000   1st Qu.:3.000  
    ##  Median :4.000   Median :5.000   Median :5.000   Median :4.000  
    ##  Mean   :3.372   Mean   :4.549   Mean   :4.399   Mean   :3.597  
    ##  3rd Qu.:4.000   3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:4.000  
    ##  Max.   :8.000   Max.   :9.000   Max.   :8.000   Max.   :9.000  
    ##  NA's   :3790    NA's   :3790    NA's   :3790    NA's   :3790   
    ##     RAPPT518        RHELP518       RDISC518        RCLFR518         RDO518     
    ##  Min.   :1.000   Min.   :1.00   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:2.00   1st Qu.:1.000   1st Qu.:2.000   1st Qu.:2.000  
    ##  Median :2.000   Median :4.00   Median :2.000   Median :3.000   Median :2.000  
    ##  Mean   :2.131   Mean   :3.36   Mean   :2.105   Mean   :2.597   Mean   :2.065  
    ##  3rd Qu.:3.000   3rd Qu.:4.00   3rd Qu.:3.000   3rd Qu.:3.000   3rd Qu.:2.000  
    ##  Max.   :8.000   Max.   :8.00   Max.   :9.000   Max.   :8.000   Max.   :8.000  
    ##  NA's   :3790    NA's   :3790   NA's   :3790    NA's   :3790    NA's   :3790   
    ##      NRFAGE           NRFSEX         NRVISIT04       NRSATVIS04   
    ##  Min.   : 0.000   Min.   : 1.000   Min.   :1.000   Min.   : 0.00  
    ##  1st Qu.: 6.000   1st Qu.: 1.000   1st Qu.:1.000   1st Qu.: 0.00  
    ##  Median :10.000   Median : 2.000   Median :2.000   Median : 5.00  
    ##  Mean   : 9.816   Mean   : 1.839   Mean   :2.603   Mean   : 9.69  
    ##  3rd Qu.:14.000   3rd Qu.: 2.000   3rd Qu.:4.000   3rd Qu.:10.00  
    ##  Max.   :18.000   Max.   :98.000   Max.   :5.000   Max.   :99.00  
    ##  NA's   :4088     NA's   :4085     NA's   :4313    NA's   :4313   
    ##     NROUTG04        NRMEAL04       NRERRAND04      NROVRNT04    
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:2.000   1st Qu.:2.000   1st Qu.:1.000   1st Qu.:1.000  
    ##  Median :3.000   Median :2.000   Median :1.000   Median :2.000  
    ##  Mean   :2.744   Mean   :2.872   Mean   :2.231   Mean   :2.333  
    ##  3rd Qu.:4.000   3rd Qu.:4.000   3rd Qu.:4.000   3rd Qu.:3.500  
    ##  Max.   :5.000   Max.   :8.000   Max.   :8.000   Max.   :5.000  
    ##  NA's   :4332    NA's   :4332    NA's   :4332    NA's   :4332   
    ##     NRPLAY04        NRREAD04       NRAFFECT04      NRPRAISE04      NRFEED04   
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.00   Min.   :1.00  
    ##  1st Qu.:2.000   1st Qu.:2.000   1st Qu.:3.000   1st Qu.:2.00   1st Qu.:2.00  
    ##  Median :3.000   Median :3.000   Median :4.000   Median :4.00   Median :4.00  
    ##  Mean   :3.205   Mean   :3.051   Mean   :3.718   Mean   :3.59   Mean   :3.59  
    ##  3rd Qu.:4.000   3rd Qu.:4.000   3rd Qu.:5.000   3rd Qu.:4.50   3rd Qu.:4.00  
    ##  Max.   :5.000   Max.   :9.000   Max.   :9.000   Max.   :9.00   Max.   :9.00  
    ##  NA's   :4332    NA's   :4332    NA's   :4332    NA's   :4332   NA's   :4332  
    ##     NRBATH04       NRDIAPER04       NRBED04         NRAPPT04    
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:2.000   1st Qu.:2.000   1st Qu.:1.000  
    ##  Median :3.000   Median :3.000   Median :2.000   Median :1.000  
    ##  Mean   :2.846   Mean   :2.923   Mean   :2.846   Mean   :1.974  
    ##  3rd Qu.:4.000   3rd Qu.:4.000   3rd Qu.:4.000   3rd Qu.:2.000  
    ##  Max.   :9.000   Max.   :9.000   Max.   :9.000   Max.   :9.000  
    ##  NA's   :4332    NA's   :4332    NA's   :4332    NA's   :4332   
    ##     NRDISC04       NRVISIT518     NRSATVIS518       NROUTG518      NRMEAL518   
    ##  Min.   :1.000   Min.   :1.000   Min.   : 0.000   Min.   :1.00   Min.   :1.00  
    ##  1st Qu.:1.000   1st Qu.:1.000   1st Qu.: 0.000   1st Qu.:2.00   1st Qu.:2.00  
    ##  Median :1.000   Median :2.000   Median : 5.000   Median :3.00   Median :3.00  
    ##  Mean   :1.615   Mean   :2.355   Mean   : 6.246   Mean   :2.62   Mean   :2.65  
    ##  3rd Qu.:2.000   3rd Qu.:3.250   3rd Qu.: 8.000   3rd Qu.:3.00   3rd Qu.:4.00  
    ##  Max.   :9.000   Max.   :8.000   Max.   :99.000   Max.   :9.00   Max.   :8.00  
    ##  NA's   :4332    NA's   :4143    NA's   :4143     NA's   :4234   NA's   :4234  
    ##   NRERRAND518      NROVRNT518     NRAFFECT518     NRPRAISE518   
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:1.000   1st Qu.:2.000   1st Qu.:3.000  
    ##  Median :2.000   Median :2.000   Median :3.000   Median :4.000  
    ##  Mean   :2.372   Mean   :2.489   Mean   :3.058   Mean   :3.591  
    ##  3rd Qu.:3.000   3rd Qu.:3.000   3rd Qu.:4.000   3rd Qu.:4.000  
    ##  Max.   :9.000   Max.   :9.000   Max.   :9.000   Max.   :8.000  
    ##  NA's   :4234    NA's   :4234    NA's   :4234    NA's   :4234   
    ##    NRTAKE518       NRAPPT518      NRHELP518       NRDISC518       NRCLFR518    
    ##  Min.   :1.000   Min.   :1.00   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:1.00   1st Qu.:1.000   1st Qu.:1.000   1st Qu.:2.000  
    ##  Median :2.000   Median :1.00   Median :2.000   Median :1.000   Median :3.000  
    ##  Mean   :2.401   Mean   :1.65   Mean   :2.467   Mean   :1.496   Mean   :3.007  
    ##  3rd Qu.:3.000   3rd Qu.:2.00   3rd Qu.:4.000   3rd Qu.:2.000   3rd Qu.:4.000  
    ##  Max.   :8.000   Max.   :8.00   Max.   :8.000   Max.   :8.000   Max.   :5.000  
    ##  NA's   :4234    NA's   :4234   NA's   :4234    NA's   :4234    NA's   :4234   
    ##     NRDO518        COPARENT         RWANT          PROBWANT        JINTEND     
    ##  Min.   :1.00   Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:2.00   1st Qu.:1.000   1st Qu.:1.000   1st Qu.:1.000   1st Qu.:1.000  
    ##  Median :3.00   Median :2.000   Median :1.000   Median :2.000   Median :5.000  
    ##  Mean   :2.73   Mean   :2.643   Mean   :2.942   Mean   :3.694   Mean   :3.334  
    ##  3rd Qu.:4.00   3rd Qu.:4.000   3rd Qu.:5.000   3rd Qu.:9.000   3rd Qu.:5.000  
    ##  Max.   :8.00   Max.   :8.000   Max.   :9.000   Max.   :9.000   Max.   :9.000  
    ##  NA's   :4234   NA's   :4085                    NA's   :4263    NA's   :3208   
    ##     JSUREINT        JINTENDN         JEXPECTL        JEXPECTS    
    ##  Min.   :1.000   Min.   : 1.000   Min.   : 1.00   Min.   :0.000  
    ##  1st Qu.:1.000   1st Qu.: 1.000   1st Qu.: 1.00   1st Qu.:0.000  
    ##  Median :1.000   Median : 2.000   Median : 3.00   Median :1.000  
    ##  Mean   :1.529   Mean   : 4.014   Mean   :32.51   Mean   :0.667  
    ##  3rd Qu.:2.000   3rd Qu.: 2.000   3rd Qu.:99.00   3rd Qu.:1.000  
    ##  Max.   :9.000   Max.   :99.000   Max.   :99.00   Max.   :2.000  
    ##  NA's   :3239    NA's   :3857     NA's   :4336    NA's   :4347   
    ##     JINTNEXT         INTEND         INTENDN          EXPECTL     
    ##  Min.   :1.000   Min.   :1.000   Min.   : 0.000   Min.   : 1.00  
    ##  1st Qu.:1.000   1st Qu.:1.000   1st Qu.: 2.000   1st Qu.: 2.00  
    ##  Median :1.000   Median :2.000   Median : 2.000   Median : 3.00  
    ##  Mean   :1.776   Mean   :1.777   Mean   : 4.712   Mean   :42.87  
    ##  3rd Qu.:2.000   3rd Qu.:2.000   3rd Qu.: 2.000   3rd Qu.:99.00  
    ##  Max.   :9.000   Max.   :9.000   Max.   :99.000   Max.   :99.00  
    ##  NA's   :3831    NA's   :2719    NA's   :2904     NA's   :4316   
    ##     EXPECTS         INTNEXT        USUALCAR        USLPLACE     
    ##  Min.   :0.000   Min.   :1.0    Min.   :1.000   Min.   : 1.000  
    ##  1st Qu.:0.000   1st Qu.:2.0    1st Qu.:1.000   1st Qu.: 1.000  
    ##  Median :1.000   Median :3.0    Median :1.000   Median : 1.000  
    ##  Mean   :0.812   Mean   :2.7    Mean   :2.198   Mean   : 3.318  
    ##  3rd Qu.:1.000   3rd Qu.:3.0    3rd Qu.:5.000   3rd Qu.: 5.000  
    ##  Max.   :2.000   Max.   :9.0    Max.   :9.000   Max.   :99.000  
    ##  NA's   :4339    NA's   :2883                   NA's   :1282    
    ##     USL12MOS        CURRCOV       COVERHOW_01      COVERHOW_02   
    ##  Min.   :1.000   Min.   :1.000   Min.   : 1.000   Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:1.000   1st Qu.: 1.000   1st Qu.:2.000  
    ##  Median :1.000   Median :1.000   Median : 1.000   Median :6.000  
    ##  Mean   :1.999   Mean   :1.618   Mean   : 3.573   Mean   :5.441  
    ##  3rd Qu.:1.000   3rd Qu.:1.000   3rd Qu.: 2.000   3rd Qu.:7.000  
    ##  Max.   :9.000   Max.   :9.000   Max.   :99.000   Max.   :9.000  
    ##  NA's   :1282                    NA's   :615      NA's   :4074   
    ##   COVERHOW_03       PARINSUR        COVER12         NUMNOCOV    
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   : 1.00  
    ##  1st Qu.:3.000   1st Qu.:1.000   1st Qu.:5.000   1st Qu.: 3.00  
    ##  Median :6.000   Median :1.000   Median :5.000   Median : 9.00  
    ##  Mean   :5.211   Mean   :1.961   Mean   :4.525   Mean   :10.09  
    ##  3rd Qu.:7.000   3rd Qu.:1.000   3rd Qu.:5.000   3rd Qu.:12.00  
    ##  Max.   :9.000   Max.   :5.000   Max.   :9.000   Max.   :99.00  
    ##  NA's   :4352    NA's   :3913                    NA's   :3766   
    ##     YOUGOFPC        WHENGOFP       YOUFPSVC_1      YOUFPSVC_2      YOUFPSVC_3  
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.00  
    ##  1st Qu.:5.000   1st Qu.:2.000   1st Qu.:1.000   1st Qu.:2.000   1st Qu.:3.00  
    ##  Median :5.000   Median :2.000   Median :2.000   Median :3.000   Median :3.00  
    ##  Mean   :4.791   Mean   :1.851   Mean   :3.065   Mean   :3.692   Mean   :4.00  
    ##  3rd Qu.:5.000   3rd Qu.:2.000   3rd Qu.:5.000   3rd Qu.:5.750   3rd Qu.:6.25  
    ##  Max.   :9.000   Max.   :9.000   Max.   :7.000   Max.   :7.000   Max.   :7.00  
    ##                  NA's   :4089    NA's   :4309    NA's   :4345    NA's   :4359  
    ##    YOUFPSVC_4      YOUFPSVC_5     YOUFPSVC_6      YOUFPSVC_7       VISION     
    ##  Min.   :2.000   Min.   :3      Min.   :6.000   Min.   :5      Min.   :1.000  
    ##  1st Qu.:4.000   1st Qu.:5      1st Qu.:6.000   1st Qu.:5      1st Qu.:1.000  
    ##  Median :4.000   Median :5      Median :6.000   Median :5      Median :1.000  
    ##  Mean   :4.167   Mean   :5      Mean   :6.333   Mean   :5      Mean   :1.288  
    ##  3rd Qu.:4.750   3rd Qu.:6      3rd Qu.:6.500   3rd Qu.:5      3rd Qu.:1.000  
    ##  Max.   :6.000   Max.   :6      Max.   :7.000   Max.   :5      Max.   :9.000  
    ##  NA's   :4365    NA's   :4366   NA's   :4368    NA's   :4370                  
    ##     HEARING         MOBILITY       COGNITION        SELFCARE    
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:1.000   1st Qu.:1.000   1st Qu.:1.000  
    ##  Median :1.000   Median :1.000   Median :1.000   Median :1.000  
    ##  Mean   :1.159   Mean   :1.124   Mean   :1.357   Mean   :1.095  
    ##  3rd Qu.:1.000   3rd Qu.:1.000   3rd Qu.:2.000   3rd Qu.:1.000  
    ##  Max.   :9.000   Max.   :9.000   Max.   :9.000   Max.   :9.000  
    ##                                                                 
    ##     COMMUNIC       EVRCANCER       AGECANCER        ALCORISK    
    ##  Min.   :1.000   Min.   :1.000   Min.   :17.00   Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:5.000   1st Qu.:22.50   1st Qu.:2.000  
    ##  Median :1.000   Median :5.000   Median :32.00   Median :3.000  
    ##  Mean   :1.136   Mean   :4.947   Mean   :32.23   Mean   :2.964  
    ##  3rd Qu.:1.000   3rd Qu.:5.000   3rd Qu.:38.50   3rd Qu.:4.000  
    ##  Max.   :9.000   Max.   :9.000   Max.   :99.00   Max.   :9.000  
    ##                                  NA's   :4300                   
    ##    VISIT12MO       SVC12MO_1       SVC12MO_2       SVC12MO_3    
    ##  Min.   :1.000   Min.   : 1.00   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:10.00   1st Qu.:2.000   1st Qu.:5.000  
    ##  Median :1.000   Median :10.00   Median :3.000   Median :7.000  
    ##  Mean   :2.283   Mean   : 8.46   Mean   :4.237   Mean   :6.159  
    ##  3rd Qu.:5.000   3rd Qu.:10.00   3rd Qu.:6.000   3rd Qu.:7.000  
    ##  Max.   :9.000   Max.   :99.00   Max.   :9.000   Max.   :9.000  
    ##                  NA's   :1371    NA's   :4130    NA's   :4258   
    ##    SVC12MO_4       SVC12MO_5       SVC12MO_6       SVC12MO_7    
    ##  Min.   :1.000   Min.   :1.000   Min.   :2.000   Min.   :4.000  
    ##  1st Qu.:6.500   1st Qu.:6.000   1st Qu.:6.000   1st Qu.:5.500  
    ##  Median :7.000   Median :7.000   Median :9.000   Median :7.000  
    ##  Mean   :7.164   Mean   :6.919   Mean   :7.273   Mean   :6.333  
    ##  3rd Qu.:9.000   3rd Qu.:9.000   3rd Qu.:9.000   3rd Qu.:7.500  
    ##  Max.   :9.000   Max.   :9.000   Max.   :9.000   Max.   :8.000  
    ##  NA's   :4304    NA's   :4334    NA's   :4360    NA's   :4368   
    ##    SVC12MO_8       SVC12MO_9       NUMVISIT       PLACEVIS_01    
    ##  Min.   :3.000   Min.   :1      Min.   : 1.000   Min.   : 1.000  
    ##  1st Qu.:5.500   1st Qu.:3      1st Qu.: 1.000   1st Qu.: 1.000  
    ##  Median :8.000   Median :5      Median : 2.000   Median : 1.000  
    ##  Mean   :6.667   Mean   :5      Mean   : 6.887   Mean   : 5.074  
    ##  3rd Qu.:8.500   3rd Qu.:7      3rd Qu.: 3.000   3rd Qu.: 4.000  
    ##  Max.   :9.000   Max.   :9      Max.   :99.000   Max.   :99.000  
    ##  NA's   :4368    NA's   :4369   NA's   :1371     NA's   :1371    
    ##   PLACEVIS_02      PLACEVIS_03      PLACEVIS_04      PLACEVIS_05  
    ##  Min.   : 1.000   Min.   : 1.000   Min.   : 1.000   Min.   :6.0   
    ##  1st Qu.: 6.000   1st Qu.: 6.000   1st Qu.: 7.000   1st Qu.:8.0   
    ##  Median : 7.000   Median : 8.000   Median : 7.000   Median :8.0   
    ##  Mean   : 7.213   Mean   : 7.869   Mean   : 8.226   Mean   :8.0   
    ##  3rd Qu.: 9.000   3rd Qu.: 9.000   3rd Qu.: 9.000   3rd Qu.:8.5   
    ##  Max.   :20.000   Max.   :20.000   Max.   :20.000   Max.   :9.0   
    ##  NA's   :3774     NA's   :4234     NA's   :4340     NA's   :4364  
    ##   PLACEVIS_06      SVCPAY_1         SVCPAY_2        SVCPAY_3    
    ##  Min.   :7.0    Min.   : 1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:7.5    1st Qu.: 1.000   1st Qu.:2.000   1st Qu.:3.000  
    ##  Median :8.0    Median : 1.000   Median :2.000   Median :3.000  
    ##  Mean   :8.0    Mean   : 3.988   Mean   :2.181   Mean   :3.035  
    ##  3rd Qu.:8.5    3rd Qu.: 2.000   3rd Qu.:2.000   3rd Qu.:3.000  
    ##  Max.   :9.0    Max.   :99.000   Max.   :6.000   Max.   :6.000  
    ##  NA's   :4369   NA's   :1371     NA's   :3099    NA's   :4169   
    ##     SVCPAY_4         TALKSA          TALKEC         TALKDM         WHYPSTD     
    ##  Min.   :4.000   Min.   :1.000   Min.   :1.00   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:4.000   1st Qu.:1.000   1st Qu.:5.00   1st Qu.:5.000   1st Qu.:1.000  
    ##  Median :4.000   Median :5.000   Median :5.00   Median :5.000   Median :4.000  
    ##  Mean   :4.667   Mean   :3.713   Mean   :4.87   Mean   :4.694   Mean   :3.393  
    ##  3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:5.00   3rd Qu.:5.000   3rd Qu.:6.000  
    ##  Max.   :6.000   Max.   :9.000   Max.   :9.00   Max.   :9.000   Max.   :9.000  
    ##  NA's   :4368    NA's   :1371    NA's   :1371   NA's   :1371    NA's   :4025   
    ##     WHYNOSTD       BARRIER_01      BARRIER_02      BARRIER_03    
    ##  Min.   :1.000   Min.   : 1.00   Min.   : 1.00   Min.   : 1.000  
    ##  1st Qu.:5.000   1st Qu.: 1.00   1st Qu.: 3.00   1st Qu.: 4.000  
    ##  Median :6.000   Median : 1.00   Median : 7.00   Median : 8.000  
    ##  Mean   :5.741   Mean   : 4.03   Mean   : 7.13   Mean   : 7.458  
    ##  3rd Qu.:7.000   3rd Qu.: 1.00   3rd Qu.:10.00   3rd Qu.:10.000  
    ##  Max.   :9.000   Max.   :99.00   Max.   :20.00   Max.   :20.000  
    ##  NA's   :1717    NA's   :3036    NA's   :4124    NA's   :4253    
    ##    BARRIER_04       BARRIER_05      BARRIER_06       BARRIER_07  
    ##  Min.   : 1.000   Min.   : 2.00   Min.   : 1.000   Min.   : 2.0  
    ##  1st Qu.: 7.000   1st Qu.: 5.75   1st Qu.: 3.750   1st Qu.: 5.5  
    ##  Median : 9.000   Median : 9.50   Median : 7.500   Median : 9.0  
    ##  Mean   : 9.235   Mean   : 8.20   Mean   : 6.667   Mean   : 7.0  
    ##  3rd Qu.:10.000   3rd Qu.:10.25   3rd Qu.: 9.750   3rd Qu.: 9.5  
    ##  Max.   :20.000   Max.   :11.00   Max.   :11.000   Max.   :10.0  
    ##  NA's   :4320     NA's   :4351    NA's   :4365     NA's   :4368  
    ##    BARRIER_08       EVERVACC       HPVSHOT1        BLDPRESS         HIGHBP     
    ##  Min.   :11.00   Min.   :1.00   Min.   : 9.00   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:13.25   1st Qu.:5.00   1st Qu.:13.00   1st Qu.:1.000   1st Qu.:5.000  
    ##  Median :15.50   Median :5.00   Median :16.00   Median :1.000   Median :5.000  
    ##  Mean   :15.50   Mean   :4.34   Mean   :26.03   Mean   :2.333   Mean   :4.349  
    ##  3rd Qu.:17.75   3rd Qu.:5.00   3rd Qu.:22.00   3rd Qu.:5.000   3rd Qu.:5.000  
    ##  Max.   :20.00   Max.   :9.00   Max.   :99.00   Max.   :9.000   Max.   :9.000  
    ##  NA's   :4369                   NA's   :3477                    NA's   :1418   
    ##      BPMEDS          BPMON         BPMONFRQ        ASKSMOKE        INFHELP     
    ##  Min.   :1.000   Min.   :1.00   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:1.00   1st Qu.:2.000   1st Qu.:1.000   1st Qu.:5.000  
    ##  Median :1.000   Median :1.00   Median :4.000   Median :1.000   Median :5.000  
    ##  Mean   :2.727   Mean   :2.83   Mean   :3.748   Mean   :2.826   Mean   :4.912  
    ##  3rd Qu.:5.000   3rd Qu.:5.00   3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:5.000  
    ##  Max.   :5.000   Max.   :5.00   Max.   :6.000   Max.   :9.000   Max.   :9.000  
    ##  NA's   :3866    NA's   :3866   NA's   :4097                    NA's   :309    
    ##    INFSVCS_1       INFSVCS_2      INFSVCS_3      INFSVCS_4       INFSVCS_5    
    ##  Min.   :1.000   Min.   :1.00   Min.   :3.00   Min.   :2.000   Min.   :5.000  
    ##  1st Qu.:1.000   1st Qu.:2.00   1st Qu.:3.00   1st Qu.:5.000   1st Qu.:7.000  
    ##  Median :2.000   Median :2.00   Median :3.00   Median :5.000   Median :7.000  
    ##  Mean   :3.035   Mean   :2.22   Mean   :3.61   Mean   :5.224   Mean   :6.857  
    ##  3rd Qu.:5.250   3rd Qu.:2.00   3rd Qu.:3.00   3rd Qu.:5.000   3rd Qu.:7.000  
    ##  Max.   :9.000   Max.   :7.00   Max.   :7.00   Max.   :7.000   Max.   :7.000  
    ##  NA's   :4143    NA's   :4244   NA's   :4289   NA's   :4322    NA's   :4357   
    ##    INFSVCS_6       INFHLPNW        LASTHELP       INFRTHIS_1     INFRTHIS_2   
    ##  Min.   :7      Min.   :1.000   Min.   :1.000   Min.   :1.00   Min.   :2.000  
    ##  1st Qu.:7      1st Qu.:5.000   1st Qu.:5.000   1st Qu.:6.00   1st Qu.:3.000  
    ##  Median :7      Median :5.000   Median :5.000   Median :6.00   Median :4.000  
    ##  Mean   :7      Mean   :4.375   Mean   :4.228   Mean   :5.36   Mean   :3.625  
    ##  3rd Qu.:7      3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:6.00   3rd Qu.:4.000  
    ##  Max.   :7      Max.   :5.000   Max.   :9.000   Max.   :9.00   Max.   :5.000  
    ##  NA's   :4370   NA's   :4179    NA's   :4143    NA's   :4143   NA's   :4363   
    ##    INFRTHIS_3      DONBLOOD       DONBLDYR        HIVTEST        WHNHIVTST    
    ##  Min.   :4      Min.   :1.00   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:4      1st Qu.:1.00   1st Qu.:5.000   1st Qu.:1.000   1st Qu.:3.000  
    ##  Median :4      Median :5.00   Median :5.000   Median :5.000   Median :4.000  
    ##  Mean   :4      Mean   :3.71   Mean   :4.316   Mean   :3.657   Mean   :3.402  
    ##  3rd Qu.:4      3rd Qu.:5.00   3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:4.000  
    ##  Max.   :4      Max.   :9.00   Max.   :5.000   Max.   :9.000   Max.   :9.000  
    ##  NA's   :4370                  NA's   :2932                    NA's   :2846   
    ##      PLCHIV          RHHIVT1        RHHIVT2_1        RHHIVT2_2   
    ##  Min.   : 1.000   Min.   :1.000   Min.   : 2.000   Min.   : 4.0  
    ##  1st Qu.: 1.000   1st Qu.:5.000   1st Qu.: 4.000   1st Qu.: 4.0  
    ##  Median : 2.000   Median :5.000   Median : 5.000   Median : 4.0  
    ##  Mean   : 4.323   Mean   :4.819   Mean   : 9.963   Mean   : 7.4  
    ##  3rd Qu.: 7.000   3rd Qu.:5.000   3rd Qu.:20.000   3rd Qu.: 5.0  
    ##  Max.   :99.000   Max.   :9.000   Max.   :20.000   Max.   :20.0  
    ##  NA's   :2846     NA's   :3874    NA's   :4344     NA's   :4366  
    ##      HIVTST          PREPHIV          PREP12         TALKDOCT    
    ##  Min.   : 1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.: 1.000   1st Qu.:1.000   1st Qu.:5.000   1st Qu.:1.000  
    ##  Median : 6.000   Median :5.000   Median :5.000   Median :5.000  
    ##  Mean   : 5.992   Mean   :3.636   Mean   :4.821   Mean   :3.976  
    ##  3rd Qu.: 8.000   3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:5.000  
    ##  Max.   :99.000   Max.   :9.000   Max.   :9.000   Max.   :9.000  
    ##  NA's   :2846                     NA's   :2843                   
    ##   AIDSTALK_01      AIDSTALK_02      AIDSTALK_03      AIDSTALK_04    
    ##  Min.   : 1.000   Min.   : 1.000   Min.   : 1.000   Min.   : 1.000  
    ##  1st Qu.: 1.000   1st Qu.: 2.000   1st Qu.: 3.000   1st Qu.: 4.000  
    ##  Median : 1.000   Median : 2.000   Median : 4.000   Median : 7.000  
    ##  Mean   : 4.316   Mean   : 3.671   Mean   : 5.234   Mean   : 6.608  
    ##  3rd Qu.: 3.000   3rd Qu.: 4.000   3rd Qu.: 8.000   3rd Qu.: 9.000  
    ##  Max.   :99.000   Max.   :20.000   Max.   :20.000   Max.   :20.000  
    ##  NA's   :3209     NA's   :3495     NA's   :3636     NA's   :3749    
    ##   AIDSTALK_05    AIDSTALK_06      AIDSTALK_07      AIDSTALK_08    
    ##  Min.   : 1.0   Min.   : 1.000   Min.   : 1.000   Min.   : 1.000  
    ##  1st Qu.: 5.0   1st Qu.: 6.000   1st Qu.: 7.000   1st Qu.: 8.000  
    ##  Median : 7.0   Median : 8.000   Median : 7.000   Median : 8.000  
    ##  Mean   : 7.2   Mean   : 7.631   Mean   : 7.701   Mean   : 8.318  
    ##  3rd Qu.: 9.0   3rd Qu.: 9.000   3rd Qu.: 9.000   3rd Qu.: 9.000  
    ##  Max.   :20.0   Max.   :20.000   Max.   :11.000   Max.   :20.000  
    ##  NA's   :3872   NA's   :3973     NA's   :4070     NA's   :4132    
    ##   AIDSTALK_09      AIDSTALK_10     AIDSTALK_11    AIDSTALK_12      SAMEADD     
    ##  Min.   : 1.000   Min.   : 1.00   Min.   : 1.0   Min.   :20     Min.   :1.000  
    ##  1st Qu.: 9.000   1st Qu.:10.00   1st Qu.:11.0   1st Qu.:20     1st Qu.:1.000  
    ##  Median : 9.000   Median :10.00   Median :11.0   Median :20     Median :1.000  
    ##  Mean   : 8.688   Mean   : 9.34   Mean   :10.2   Mean   :20     Mean   :2.482  
    ##  3rd Qu.:10.000   3rd Qu.:10.00   3rd Qu.:11.0   3rd Qu.:20     3rd Qu.:5.000  
    ##  Max.   :20.000   Max.   :20.00   Max.   :20.0   Max.   :20     Max.   :9.000  
    ##  NA's   :4182     NA's   :4224    NA's   :4273   NA's   :4367                  
    ##      BRNOUT         ATTND14         FUNDAM_1        FUNDAM_2    
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:5.000   1st Qu.:2.000   1st Qu.:1.000   1st Qu.:2.000  
    ##  Median :5.000   Median :5.000   Median :5.000   Median :3.000  
    ##  Mean   :4.416   Mean   :4.432   Mean   :3.618   Mean   :2.483  
    ##  3rd Qu.:5.000   3rd Qu.:7.000   3rd Qu.:5.000   3rd Qu.:3.000  
    ##  Max.   :9.000   Max.   :9.000   Max.   :9.000   Max.   :4.000  
    ##                  NA's   :3215    NA's   :2070    NA's   :4311   
    ##     FUNDAM_3        FUNDAM_4       RELDLIFE        ATTNDNOW         MILSVC     
    ##  Min.   :1.000   Min.   :4      Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:3.000   1st Qu.:4      1st Qu.:1.000   1st Qu.:4.000   1st Qu.:2.000  
    ##  Median :3.000   Median :4      Median :2.000   Median :6.000   Median :2.000  
    ##  Mean   :2.611   Mean   :4      Mean   :1.858   Mean   :5.406   Mean   :1.982  
    ##  3rd Qu.:3.000   3rd Qu.:4      3rd Qu.:2.000   3rd Qu.:7.000   3rd Qu.:2.000  
    ##  Max.   :3.000   Max.   :4      Max.   :9.000   Max.   :9.000   Max.   :9.000  
    ##  NA's   :4353    NA's   :4367   NA's   :1726                    NA's   :393    
    ##     WRK12MOS        FPT12MOS       DOLASTWK1       DOLASTWK2    
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:1.000   1st Qu.:1.000   1st Qu.:4.000  
    ##  Median :1.000   Median :1.000   Median :1.000   Median :5.000  
    ##  Mean   :1.861   Mean   :1.335   Mean   :2.072   Mean   :4.372  
    ##  3rd Qu.:1.000   3rd Qu.:1.000   3rd Qu.:3.000   3rd Qu.:5.000  
    ##  Max.   :9.000   Max.   :9.000   Max.   :9.000   Max.   :6.000  
    ##                  NA's   :914                     NA's   :3440   
    ##    DOLASTWK3       DOLASTWK4       DOLASTWK5      DOLASTWK6        RWRKST     
    ##  Min.   :1.000   Min.   :3.000   Min.   :6      Min.   :2      Min.   :1.000  
    ##  1st Qu.:5.000   1st Qu.:5.000   1st Qu.:6      1st Qu.:2      1st Qu.:1.000  
    ##  Median :5.000   Median :6.000   Median :6      Median :2      Median :1.000  
    ##  Mean   :4.974   Mean   :5.222   Mean   :6      Mean   :2      Mean   :2.099  
    ##  3rd Qu.:6.000   3rd Qu.:6.000   3rd Qu.:6      3rd Qu.:2      3rd Qu.:5.000  
    ##  Max.   :6.000   Max.   :6.000   Max.   :6      Max.   :2      Max.   :5.000  
    ##  NA's   :4220    NA's   :4353    NA's   :4370   NA's   :4370                  
    ##      RFTPTX       SPLSTWK1        SPLSTWK2        SPLSTWK3        SPLSTWK4   
    ##  Min.   :1.0   Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.00  
    ##  1st Qu.:2.0   1st Qu.:1.000   1st Qu.:4.000   1st Qu.:4.000   1st Qu.:3.50  
    ##  Median :2.0   Median :1.000   Median :5.000   Median :5.000   Median :4.50  
    ##  Mean   :1.8   Mean   :2.257   Mean   :4.442   Mean   :4.821   Mean   :4.25  
    ##  3rd Qu.:2.0   3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:6.000   3rd Qu.:6.00  
    ##  Max.   :9.0   Max.   :9.000   Max.   :6.000   Max.   :6.000   Max.   :6.00  
    ##  NA's   :742   NA's   :2559    NA's   :3968    NA's   :4315    NA's   :4363  
    ##     SPLSTWK5       SPLSTWK6       SPWRKST         SPFTPTX         REACTSLF    
    ##  Min.   :5      Min.   :6      Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:5      1st Qu.:6      1st Qu.:1.000   1st Qu.:2.000   1st Qu.:2.000  
    ##  Median :5      Median :6      Median :1.000   Median :2.000   Median :3.000  
    ##  Mean   :5      Mean   :6      Mean   :2.141   Mean   :1.816   Mean   :3.219  
    ##  3rd Qu.:5      3rd Qu.:6      3rd Qu.:5.000   3rd Qu.:2.000   3rd Qu.:5.000  
    ##  Max.   :5      Max.   :6      Max.   :5.000   Max.   :9.000   Max.   :9.000  
    ##  NA's   :4370   NA's   :4370   NA's   :2559    NA's   :3076    NA's   :875    
    ##     CHBOTHER       SEXNEEDS        WHENSICK        SHOWPAIN       CASILANG    
    ##  Min.   :1.00   Min.   :1.000   Min.   :1.000   Min.   :1.00   Min.   :1.000  
    ##  1st Qu.:2.00   1st Qu.:2.000   1st Qu.:3.000   1st Qu.:3.00   1st Qu.:1.000  
    ##  Median :4.00   Median :3.000   Median :3.000   Median :3.00   Median :1.000  
    ##  Mean   :3.24   Mean   :3.306   Mean   :3.235   Mean   :3.35   Mean   :1.031  
    ##  3rd Qu.:4.00   3rd Qu.:5.000   3rd Qu.:4.000   3rd Qu.:4.00   3rd Qu.:1.000  
    ##  Max.   :9.00   Max.   :9.000   Max.   :9.000   Max.   :9.00   Max.   :2.000  
    ##                                                                               
    ##     GENHEALT         BMIcat         DRWEIGH         TELLWGHT    
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:2.000   1st Qu.:2.000   1st Qu.:1.000   1st Qu.:2.000  
    ##  Median :2.000   Median :3.000   Median :1.000   Median :3.000  
    ##  Mean   :2.342   Mean   :3.031   Mean   :2.449   Mean   :3.004  
    ##  3rd Qu.:3.000   3rd Qu.:4.000   3rd Qu.:5.000   3rd Qu.:4.000  
    ##  Max.   :9.000   Max.   :5.000   Max.   :9.000   Max.   :9.000  
    ##  NA's   :3       NA's   :699     NA's   :4       NA's   :1522   
    ##     WGHTSCRN        ENGSPEAK        NOBEDYR         STAYREL     
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:5.000   1st Qu.:1.000   1st Qu.:5.000   1st Qu.:5.000  
    ##  Median :5.000   Median :1.000   Median :5.000   Median :5.000  
    ##  Mean   :4.052   Mean   :1.225   Mean   :4.868   Mean   :4.841  
    ##  3rd Qu.:5.000   3rd Qu.:1.000   3rd Qu.:5.000   3rd Qu.:5.000  
    ##  Max.   :9.000   Max.   :9.000   Max.   :9.000   Max.   :9.000  
    ##  NA's   :2881    NA's   :5       NA's   :6       NA's   :6      
    ##      JAILED         JAILED2         FRQJAIL         FRQJAIL2        EVSUSPEN   
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.00  
    ##  1st Qu.:5.000   1st Qu.:5.000   1st Qu.:1.000   1st Qu.:1.000   1st Qu.:5.00  
    ##  Median :5.000   Median :5.000   Median :2.000   Median :1.000   Median :5.00  
    ##  Mean   :4.934   Mean   :4.557   Mean   :1.566   Mean   :1.758   Mean   :4.04  
    ##  3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:2.000   3rd Qu.:2.000   3rd Qu.:5.00  
    ##  Max.   :9.000   Max.   :9.000   Max.   :9.000   Max.   :9.000   Max.   :9.00  
    ##  NA's   :6       NA's   :107     NA's   :3763    NA's   :3763    NA's   :3216  
    ##     GRADSUSP         SMK100          AGESMK         SMOKE30        DRINK12     
    ##  Min.   : 1.00   Min.   :1.000   Min.   :11.00   Min.   :1.00   Min.   :1.000  
    ##  1st Qu.: 6.00   1st Qu.:1.000   1st Qu.:16.00   1st Qu.:1.00   1st Qu.:1.000  
    ##  Median : 8.00   Median :5.000   Median :18.00   Median :1.00   Median :3.000  
    ##  Mean   :12.04   Mean   :3.908   Mean   :31.61   Mean   :2.35   Mean   :3.232  
    ##  3rd Qu.:10.00   3rd Qu.:5.000   3rd Qu.:23.00   3rd Qu.:4.00   3rd Qu.:5.000  
    ##  Max.   :99.00   Max.   :9.000   Max.   :99.00   Max.   :9.00   Max.   :9.000  
    ##  NA's   :4084    NA's   :7       NA's   :3138    NA's   :3138   NA's   :8      
    ##     BINGE12          POT12          FEMTOUCH         VAGSEX     
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:1.000   1st Qu.:1.000   1st Qu.:1.000  
    ##  Median :2.000   Median :1.000   Median :5.000   Median :5.000  
    ##  Mean   :2.499   Mean   :2.102   Mean   :3.916   Mean   :3.134  
    ##  3rd Qu.:4.000   3rd Qu.:3.000   3rd Qu.:5.000   3rd Qu.:5.000  
    ##  Max.   :9.000   Max.   :9.000   Max.   :9.000   Max.   :9.000  
    ##  NA's   :1265    NA's   :8       NA's   :3694    NA's   :3832   
    ##     AGEVAGR         CONDVAG         COND1BRK        COND1OFF       WHYCONDL    
    ##  Min.   :10.00   Min.   :1.000   Min.   :1.000   Min.   :1.00   Min.   :1.000  
    ##  1st Qu.:15.00   1st Qu.:1.000   1st Qu.:5.000   1st Qu.:5.00   1st Qu.:1.000  
    ##  Median :17.00   Median :5.000   Median :5.000   Median :5.00   Median :3.000  
    ##  Mean   :26.84   Mean   :3.768   Mean   :4.931   Mean   :4.53   Mean   :2.262  
    ##  3rd Qu.:19.00   3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:5.00   3rd Qu.:3.000  
    ##  Max.   :99.00   Max.   :9.000   Max.   :9.000   Max.   :9.00   Max.   :9.000  
    ##  NA's   :4103    NA's   :1023    NA's   :3283    NA's   :3283   NA's   :3283   
    ##     GETORALF        CONDFELL       GIVORALF        ANYORAL         K_HADSEX    
    ##  Min.   :1.000   Min.   :1.0    Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:5.0    1st Qu.:1.000   1st Qu.:1.000   1st Qu.:1.000  
    ##  Median :1.000   Median :5.0    Median :1.000   Median :1.000   Median :1.000  
    ##  Mean   :2.352   Mean   :4.8    Mean   :2.482   Mean   :2.099   Mean   :1.928  
    ##  3rd Qu.:5.000   3rd Qu.:5.0    3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:1.000  
    ##  Max.   :9.000   Max.   :9.0    Max.   :9.000   Max.   :5.000   Max.   :5.000  
    ##  NA's   :12      NA's   :1396   NA's   :12      NA's   :124     NA's   :1      
    ##      TIMING         ANALSEX         CONDANAL      OPPSEXANY       OPPSEXGEN    
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.00   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:1.000   1st Qu.:5.00   1st Qu.:1.000   1st Qu.:1.000  
    ##  Median :3.000   Median :5.000   Median :5.00   Median :1.000   Median :1.000  
    ##  Mean   :3.052   Mean   :3.839   Mean   :4.13   Mean   :1.798   Mean   :1.806  
    ##  3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:5.00   3rd Qu.:1.000   3rd Qu.:1.000  
    ##  Max.   :9.000   Max.   :9.000   Max.   :9.00   Max.   :5.000   Max.   :5.000  
    ##  NA's   :3907    NA's   :12      NA's   :3028   NA's   :37      NA's   :37     
    ##     CONDSEXL       OPPLIFENUM       OPPYEARNUM        VAGNUM12     
    ##  Min.   :1.000   Min.   :  1.00   Min.   :  0.00   Min.   :  0.00  
    ##  1st Qu.:1.000   1st Qu.:  2.00   1st Qu.:  1.00   1st Qu.:  1.00  
    ##  Median :1.000   Median :  5.00   Median :  1.00   Median :  1.00  
    ##  Mean   :1.922   Mean   : 79.28   Mean   : 44.06   Mean   : 34.99  
    ##  3rd Qu.:1.000   3rd Qu.: 15.00   3rd Qu.:  1.00   3rd Qu.:  1.00  
    ##  Max.   :9.000   Max.   :999.00   Max.   :999.00   Max.   :999.00  
    ##  NA's   :3248    NA's   :920      NA's   :920      NA's   :1596    
    ##    ORALNUM12       ANALNUM12        RNONMONOG        NONMONOG    
    ##  Min.   :  0.0   Min.   :  0.00   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:  1.0   1st Qu.:  0.00   1st Qu.:1.000   1st Qu.:5.000  
    ##  Median :  1.0   Median :  0.00   Median :5.000   Median :5.000  
    ##  Mean   : 29.9   Mean   : 16.66   Mean   :3.409   Mean   :4.834  
    ##  3rd Qu.:  1.0   3rd Qu.:  1.00   3rd Qu.:5.000   3rd Qu.:5.000  
    ##  Max.   :999.0   Max.   :999.00   Max.   :9.000   Max.   :9.000  
    ##  NA's   :1791    NA's   :3188     NA's   :3892    NA's   :1539   
    ##    NNONMONOG         FEMSHT12        JOHNFREQ        PROSTFRQ    
    ##  Min.   :  0.00   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:  1.00   1st Qu.:5.000   1st Qu.:5.000   1st Qu.:5.000  
    ##  Median :  2.00   Median :5.000   Median :5.000   Median :5.000  
    ##  Mean   : 66.86   Mean   :5.032   Mean   :5.003   Mean   :5.006  
    ##  3rd Qu.:  3.00   3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:5.000  
    ##  Max.   :999.00   Max.   :9.000   Max.   :9.000   Max.   :9.000  
    ##  NA's   :4187     NA's   :1484    NA's   :1486    NA's   :1486   
    ##     GIVORALM        GETORALM       ORALCONDM        ANALSEX2    
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:5.000   1st Qu.:5.000   1st Qu.:5.000   1st Qu.:5.000  
    ##  Median :5.000   Median :5.000   Median :5.000   Median :5.000  
    ##  Mean   :4.746   Mean   :4.727   Mean   :4.518   Mean   :4.818  
    ##  3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:5.000  
    ##  Max.   :9.000   Max.   :9.000   Max.   :8.000   Max.   :9.000  
    ##  NA's   :27      NA's   :27      NA's   :4004    NA's   :27     
    ##    ANALCONDM1       ANALSEX3       ANALCONDM2       MALESEX     
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:5.000   1st Qu.:1.000   1st Qu.:5.000  
    ##  Median :5.000   Median :5.000   Median :5.000   Median :5.000  
    ##  Mean   :3.625   Mean   :4.828   Mean   :3.559   Mean   :4.827  
    ##  3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:5.000  
    ##  Max.   :8.000   Max.   :9.000   Max.   :5.000   Max.   :9.000  
    ##  NA's   :4123    NA's   :28      NA's   :4135    NA's   :28     
    ##    SAMESEXANY      MALPRTAGE       SAMLIFENUM       SAMYEARNUM    
    ##  Min.   :1.000   Min.   :1.000   Min.   :  1.00   Min.   :  0.00  
    ##  1st Qu.:5.000   1st Qu.:1.000   1st Qu.:  1.00   1st Qu.:  0.00  
    ##  Median :5.000   Median :2.000   Median :  5.00   Median :  1.00  
    ##  Mean   :4.626   Mean   :2.258   Mean   : 70.29   Mean   : 34.19  
    ##  3rd Qu.:5.000   3rd Qu.:3.000   3rd Qu.: 10.00   3rd Qu.:  2.00  
    ##  Max.   :5.000   Max.   :9.000   Max.   :999.00   Max.   :999.00  
    ##  NA's   :101     NA's   :3972    NA's   :3974     NA's   :3974    
    ##    SAMORAL12       RECEPANAL12      INSERANAL12        SAMESEX1     
    ##  Min.   :  0.00   Min.   :  0.00   Min.   :  0.00   Min.   : 1.000  
    ##  1st Qu.:  1.00   1st Qu.:  1.00   1st Qu.:  1.00   1st Qu.: 2.000  
    ##  Median :  2.00   Median :  1.00   Median :  1.00   Median : 2.000  
    ##  Mean   : 40.18   Mean   : 24.84   Mean   : 30.85   Mean   : 6.484  
    ##  3rd Qu.:  5.00   3rd Qu.:  3.00   3rd Qu.:  3.00   3rd Qu.: 3.000  
    ##  Max.   :999.00   Max.   :999.00   Max.   :999.00   Max.   :99.000  
    ##  NA's   :4158     NA's   :4197     NA's   :4199     NA's   :3974    
    ##     MSAMEREL       MALEGSTAT        MALMARRN        MALCOHN     
    ##  Min.   : 1.00   Min.   :3.000   Min.   :1.000   Min.   :0.000  
    ##  1st Qu.: 7.00   1st Qu.:5.000   1st Qu.:1.000   1st Qu.:0.000  
    ##  Median : 7.00   Median :5.000   Median :1.000   Median :0.000  
    ##  Mean   : 9.25   Mean   :5.023   Mean   :1.178   Mean   :1.206  
    ##  3rd Qu.: 8.00   3rd Qu.:5.000   3rd Qu.:1.000   3rd Qu.:1.000  
    ##  Max.   :99.00   Max.   :9.000   Max.   :5.000   Max.   :9.000  
    ##  NA's   :3975    NA's   :4021    NA's   :4326    NA's   :3987   
    ##    MSMNONMON         MALSHT12        JOHN2FRQ        PROS2FRQ    
    ##  Min.   :  0.00   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:  0.00   1st Qu.:5.000   1st Qu.:5.000   1st Qu.:5.000  
    ##  Median :  1.00   Median :5.000   Median :5.000   Median :5.000  
    ##  Mean   : 76.17   Mean   :4.847   Mean   :4.898   Mean   :4.828  
    ##  3rd Qu.:  5.00   3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:5.000  
    ##  Max.   :999.00   Max.   :9.000   Max.   :9.000   Max.   :9.000  
    ##  NA's   :4156     NA's   :4156    NA's   :4156    NA's   :4156   
    ##    MSMSORT12        CNDLSMAL        CONDALLS        MFLASTP     
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:5.000   1st Qu.:1.000   1st Qu.:1.000  
    ##  Median :1.000   Median :5.000   Median :5.000   Median :2.000  
    ##  Mean   :2.298   Mean   :4.232   Mean   :4.149   Mean   :1.798  
    ##  3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:2.000  
    ##  Max.   :9.000   Max.   :9.000   Max.   :9.000   Max.   :9.000  
    ##  NA's   :4156    NA's   :3975    NA's   :4277    NA's   :4277   
    ##     WHYCOND         DATEAPP         ATTRACT          ORIENT     
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:1.500   1st Qu.:5.000   1st Qu.:1.000   1st Qu.:2.000  
    ##  Median :3.000   Median :5.000   Median :1.000   Median :2.000  
    ##  Mean   :2.444   Mean   :4.697   Mean   :1.568   Mean   :2.169  
    ##  3rd Qu.:3.000   3rd Qu.:5.000   3rd Qu.:1.000   3rd Qu.:2.000  
    ##  Max.   :3.000   Max.   :9.000   Max.   :9.000   Max.   :9.000  
    ##  NA's   :4353    NA's   :759     NA's   :31      NA's   :31     
    ##     CONFCONC        TIMALON        RISKCHEK1       RISKCHEK2       RISKCHEK3  
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.0  
    ##  1st Qu.:5.000   1st Qu.:1.000   1st Qu.:5.000   1st Qu.:5.000   1st Qu.:5.0  
    ##  Median :5.000   Median :5.000   Median :5.000   Median :5.000   Median :5.0  
    ##  Mean   :4.889   Mean   :3.615   Mean   :4.544   Mean   :4.641   Mean   :4.6  
    ##  3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:5.0  
    ##  Max.   :9.000   Max.   :9.000   Max.   :9.000   Max.   :9.000   Max.   :9.0  
    ##  NA's   :3113    NA's   :3979    NA's   :33      NA's   :34      NA's   :34   
    ##    RISKCHEK4       RECTDOUCH        STDTST12       STDSITE12    
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:5.000   1st Qu.:1.000   1st Qu.:5.000   1st Qu.:1.000  
    ##  Median :5.000   Median :2.000   Median :5.000   Median :5.000  
    ##  Mean   :4.804   Mean   :2.647   Mean   :4.626   Mean   :3.883  
    ##  3rd Qu.:5.000   3rd Qu.:4.000   3rd Qu.:5.000   3rd Qu.:5.000  
    ##  Max.   :9.000   Max.   :9.000   Max.   :9.000   Max.   :9.000  
    ##  NA's   :34      NA's   :4204    NA's   :34      NA's   :3884   
    ##     STDTRT12          GON            CHLAM           HERPES     
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:5.000   1st Qu.:5.000   1st Qu.:5.000   1st Qu.:5.000  
    ##  Median :5.000   Median :5.000   Median :5.000   Median :5.000  
    ##  Mean   :4.976   Mean   :5.028   Mean   :5.031   Mean   :4.983  
    ##  3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:5.000  
    ##  Max.   :9.000   Max.   :9.000   Max.   :9.000   Max.   :9.000  
    ##  NA's   :34      NA's   :34      NA's   :34      NA's   :34     
    ##     GENWARTS        SYPHILIS       EMOTABUSE       PHYSABUSE    
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:5.000   1st Qu.:5.000   1st Qu.:1.000   1st Qu.:1.000  
    ##  Median :5.000   Median :5.000   Median :2.000   Median :1.000  
    ##  Mean   :4.994   Mean   :5.007   Mean   :2.235   Mean   :1.753  
    ##  3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:3.000   3rd Qu.:2.000  
    ##  Max.   :9.000   Max.   :9.000   Max.   :9.000   Max.   :9.000  
    ##  NA's   :34      NA's   :35      NA's   :43      NA's   :45     
    ##     SEXABUSE       REVPHYSNEG      REVEMOTNEG      WITNESSIPV   
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:5.000   1st Qu.:4.000   1st Qu.:1.000  
    ##  Median :1.000   Median :5.000   Median :5.000   Median :1.000  
    ##  Mean   :1.255   Mean   :4.536   Mean   :4.477   Mean   :1.489  
    ##  3rd Qu.:1.000   3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:1.000  
    ##  Max.   :9.000   Max.   :9.000   Max.   :9.000   Max.   :9.000  
    ##  NA's   :438     NA's   :46      NA's   :46      NA's   :48     
    ##     LIVDRUGS       LIVDEPRESS       SEPJAIL       RACEDESCRIM   
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:5.000   1st Qu.:5.000   1st Qu.:5.000   1st Qu.:1.000  
    ##  Median :5.000   Median :5.000   Median :5.000   Median :1.000  
    ##  Mean   :4.344   Mean   :4.297   Mean   :4.843   Mean   :1.598  
    ##  3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:2.000  
    ##  Max.   :9.000   Max.   :9.000   Max.   :9.000   Max.   :9.000  
    ##  NA's   :48      NA's   :48      NA's   :48      NA's   :48     
    ##   GENDDESCRIM       WITVIOL         EARNTYPE          EARN      
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   : 1.00  
    ##  1st Qu.:1.000   1st Qu.:1.000   1st Qu.:2.000   1st Qu.: 8.00  
    ##  Median :1.000   Median :1.000   Median :3.000   Median :12.00  
    ##  Mean   :1.365   Mean   :1.538   Mean   :2.764   Mean   :15.26  
    ##  3rd Qu.:1.000   3rd Qu.:2.000   3rd Qu.:3.000   3rd Qu.:15.00  
    ##  Max.   :9.000   Max.   :9.000   Max.   :9.000   Max.   :99.00  
    ##  NA's   :48      NA's   :48      NA's   :947     NA's   :947    
    ##     EARNDK1         EARNDK2         EARNDK3        EARNDK4        TOINCWMY    
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.0    Min.   :8      Min.   :1.000  
    ##  1st Qu.:5.000   1st Qu.:1.000   1st Qu.:5.0    1st Qu.:8      1st Qu.:2.000  
    ##  Median :8.000   Median :5.000   Median :6.5    Median :8      Median :3.000  
    ##  Mean   :6.508   Mean   :5.029   Mean   :5.7    Mean   :8      Mean   :3.275  
    ##  3rd Qu.:8.000   3rd Qu.:8.000   3rd Qu.:8.0    3rd Qu.:8      3rd Qu.:3.000  
    ##  Max.   :9.000   Max.   :9.000   Max.   :8.0    Max.   :8      Max.   :9.000  
    ##  NA's   :4190    NA's   :4336    NA's   :4361   NA's   :4369   NA's   :54     
    ##      TOTINC        FMINCDK1        FMINCDK2       FMINCDK3        FMINCDK4    
    ##  Min.   : 1.0   Min.   :1.000   Min.   :1.00   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:11.0   1st Qu.:5.000   1st Qu.:1.00   1st Qu.:1.000   1st Qu.:1.000  
    ##  Median :14.0   Median :8.000   Median :5.00   Median :1.000   Median :5.000  
    ##  Mean   :21.7   Mean   :6.963   Mean   :4.88   Mean   :3.154   Mean   :4.857  
    ##  3rd Qu.:15.0   3rd Qu.:9.000   3rd Qu.:9.00   3rd Qu.:5.000   3rd Qu.:9.000  
    ##  Max.   :99.0   Max.   :9.000   Max.   :9.00   Max.   :9.000   Max.   :9.000  
    ##  NA's   :54     NA's   :3885    NA's   :4296   NA's   :4345    NA's   :4308   
    ##     FMINCDK5        PUBASST         FOODSTMP          WIC           HLPTRANS   
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.00  
    ##  1st Qu.:1.000   1st Qu.:5.000   1st Qu.:5.000   1st Qu.:5.000   1st Qu.:5.00  
    ##  Median :5.000   Median :5.000   Median :5.000   Median :5.000   Median :5.00  
    ##  Mean   :4.926   Mean   :5.045   Mean   :4.675   Mean   :5.026   Mean   :5.11  
    ##  3rd Qu.:8.000   3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:5.00  
    ##  Max.   :9.000   Max.   :9.000   Max.   :9.000   Max.   :9.000   Max.   :9.00  
    ##  NA's   :4344    NA's   :54      NA's   :55      NA's   :55      NA's   :56    
    ##     HLPCHLDC         HLPJOB         FREEFOOD         HUNGRY     
    ##  Min.   :1.000   Min.   :1.000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:5.000   1st Qu.:5.000   1st Qu.:5.000   1st Qu.:5.000  
    ##  Median :5.000   Median :5.000   Median :5.000   Median :5.000  
    ##  Mean   :5.122   Mean   :5.109   Mean   :4.995   Mean   :4.886  
    ##  3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.:5.000  
    ##  Max.   :9.000   Max.   :9.000   Max.   :9.000   Max.   :9.000  
    ##  NA's   :58      NA's   :58      NA's   :58      NA's   :60     
    ##     MED_COST        COVIDVAX        COVVAX_M        COVVAX_Y       CMCOVVAX   
    ##  Min.   :1.000   Min.   :1.000   Min.   : 1.00   Min.   :2020   Min.   :1441  
    ##  1st Qu.:5.000   1st Qu.:1.000   1st Qu.: 3.00   1st Qu.:2021   1st Qu.:1454  
    ##  Median :5.000   Median :1.000   Median : 5.00   Median :2021   Median :1456  
    ##  Mean   :4.859   Mean   :2.153   Mean   : 7.88   Mean   :2132   Mean   :1575  
    ##  3rd Qu.:5.000   3rd Qu.:5.000   3rd Qu.: 8.00   3rd Qu.:2021   3rd Qu.:1459  
    ##  Max.   :9.000   Max.   :9.000   Max.   :99.00   Max.   :9999   Max.   :9999  
    ##  NA's   :60      NA's   :60      NA's   :1204    NA's   :1204   NA's   :1204  
    ##     HADCOVID          AGER          FMARITAL        RMARITAL    
    ##  Min.   :1.000   Min.   :15.00   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:24.00   1st Qu.:1.000   1st Qu.:1.000  
    ##  Median :5.000   Median :32.00   Median :5.000   Median :6.000  
    ##  Mean   :3.208   Mean   :31.78   Mean   :3.641   Mean   :4.011  
    ##  3rd Qu.:5.000   3rd Qu.:40.00   3rd Qu.:5.000   3rd Qu.:6.000  
    ##  Max.   :9.000   Max.   :50.00   Max.   :5.000   Max.   :6.000  
    ##  NA's   :63                                                     
    ##      HIEDUC          HIEDUC_I           HISPANIC     HISPANIC_I      
    ##  Min.   : 1.000   Min.   :0.000000   Min.   :1.0   Min.   :0.000000  
    ##  1st Qu.: 4.000   1st Qu.:0.000000   1st Qu.:2.0   1st Qu.:0.000000  
    ##  Median : 5.000   Median :0.000000   Median :2.0   Median :0.000000  
    ##  Mean   : 5.507   Mean   :0.003661   Mean   :1.8   Mean   :0.003661  
    ##  3rd Qu.: 8.000   3rd Qu.:0.000000   3rd Qu.:2.0   3rd Qu.:0.000000  
    ##  Max.   :11.000   Max.   :2.000000   Max.   :2.0   Max.   :2.000000  
    ##                                                                      
    ##    HISPRACE2      HISPRACE2_I          NUMKDHH          NUMFMHH     
    ##  Min.   :1.000   Min.   :0.000000   Min.   :0.0000   Min.   :0.000  
    ##  1st Qu.:2.000   1st Qu.:0.000000   1st Qu.:0.0000   1st Qu.:0.000  
    ##  Median :2.000   Median :0.000000   Median :0.0000   Median :1.000  
    ##  Mean   :2.202   Mean   :0.005033   Mean   :0.4891   Mean   :1.659  
    ##  3rd Qu.:3.000   3rd Qu.:0.000000   3rd Qu.:1.0000   3rd Qu.:3.000  
    ##  Max.   :4.000   Max.   :2.000000   Max.   :4.0000   Max.   :6.000  
    ##                                                                     
    ##     HHFAMTYP       HHFAMTYP_I    HHPARTYP       NCHILDHH         HHKIDTYP     
    ##  Min.   :1.000   Min.   :0    Min.   :1.00   Min.   :0.0000   Min.   :0.0000  
    ##  1st Qu.:1.000   1st Qu.:0    1st Qu.:3.00   1st Qu.:0.0000   1st Qu.:0.0000  
    ##  Median :1.000   Median :0    Median :4.00   Median :0.0000   Median :0.0000  
    ##  Mean   :1.763   Mean   :0    Mean   :3.33   Mean   :0.4823   Mean   :0.2906  
    ##  3rd Qu.:3.000   3rd Qu.:0    3rd Qu.:4.00   3rd Qu.:1.0000   3rd Qu.:1.0000  
    ##  Max.   :5.000   Max.   :0    Max.   :4.00   Max.   :3.0000   Max.   :2.0000  
    ##                                                                               
    ##     CSPBBHH          CSPSBHH          CSPOKDHH         INTCTFAM    
    ##  Min.   :0.0000   Min.   :0.0000   Min.   :0.0000   Min.   :1.000  
    ##  1st Qu.:0.0000   1st Qu.:0.0000   1st Qu.:0.0000   1st Qu.:1.000  
    ##  Median :1.0000   Median :0.0000   Median :0.0000   Median :1.000  
    ##  Mean   :0.9988   Mean   :0.0564   Mean   :0.0368   Mean   :1.295  
    ##  3rd Qu.:2.0000   3rd Qu.:0.0000   3rd Qu.:0.0000   3rd Qu.:2.000  
    ##  Max.   :3.0000   Max.   :1.0000   Max.   :1.0000   Max.   :2.000  
    ##  NA's   :2634     NA's   :2634     NA's   :2634                    
    ##    INTCTFAM_I         PARAGE14       PARAGE14_I          EDUCMOM      
    ##  Min.   :0.00000   Min.   :1.000   Min.   :0.000000   Min.   : 1.000  
    ##  1st Qu.:0.00000   1st Qu.:1.000   1st Qu.:0.000000   1st Qu.: 2.000  
    ##  Median :0.00000   Median :1.000   Median :0.000000   Median : 3.000  
    ##  Mean   :0.00183   Mean   :1.406   Mean   :0.006863   Mean   : 3.967  
    ##  3rd Qu.:0.00000   3rd Qu.:1.000   3rd Qu.:0.000000   3rd Qu.: 4.000  
    ##  Max.   :1.00000   Max.   :3.000   Max.   :2.000000   Max.   :95.000  
    ##                                                                       
    ##    EDUCMOM_I          AGEMOMB1        AGEMOMB1_I          HADSEX     
    ##  Min.   :0.00000   Min.   : 1.000   Min.   :0.00000   Min.   :1.000  
    ##  1st Qu.:0.00000   1st Qu.: 3.000   1st Qu.:0.00000   1st Qu.:1.000  
    ##  Median :0.00000   Median : 3.000   Median :0.00000   Median :1.000  
    ##  Mean   :0.02219   Mean   : 5.567   Mean   :0.03043   Mean   :1.231  
    ##  3rd Qu.:0.00000   3rd Qu.: 4.000   3rd Qu.:0.00000   3rd Qu.:1.000  
    ##  Max.   :2.00000   Max.   :96.000   Max.   :2.00000   Max.   :2.000  
    ##                                                                      
    ##     LSEXDATE      LSEXDATE_I         lsexrage        sex3mo     
    ##  Min.   :1043   Min.   :0.00000   Min.   :10     Min.   :1.000  
    ##  1st Qu.:1468   1st Qu.:0.00000   1st Qu.:26     1st Qu.:1.000  
    ##  Median :1476   Median :0.00000   Median :33     Median :1.000  
    ##  Mean   :1466   Mean   :0.01716   Mean   :33     Mean   :1.305  
    ##  3rd Qu.:1481   3rd Qu.:0.00000   3rd Qu.:40     3rd Qu.:2.000  
    ##  Max.   :9997   Max.   :2.00000   Max.   :50     Max.   :2.000  
    ##  NA's   :1009                     NA's   :1009   NA's   :1009   
    ##     sex12mo         LSEXRLTN       LSEXRLTN_I         LSEXUSE1    
    ##  Min.   :1.000   Min.   :1.000   Min.   :0.00000   Min.   : 1.00  
    ##  1st Qu.:1.000   1st Qu.:1.000   1st Qu.:0.00000   1st Qu.: 1.00  
    ##  Median :1.000   Median :3.000   Median :0.00000   Median : 4.00  
    ##  Mean   :1.183   Mean   :3.201   Mean   :0.02059   Mean   :35.43  
    ##  3rd Qu.:1.000   3rd Qu.:4.000   3rd Qu.:0.00000   3rd Qu.:96.00  
    ##  Max.   :2.000   Max.   :9.000   Max.   :2.00000   Max.   :96.00  
    ##  NA's   :1009    NA's   :1009                      NA's   :1009   
    ##    LSEXUSE1_I         LSEXUSE2       LSEXUSE2_I         LSEXUSE3    
    ##  Min.   :0.00000   Min.   : 1.00   Min.   :0.00000   Min.   : 1.00  
    ##  1st Qu.:0.00000   1st Qu.: 4.00   1st Qu.:0.00000   1st Qu.:96.00  
    ##  Median :0.00000   Median :96.00   Median :0.00000   Median :96.00  
    ##  Mean   :0.01418   Mean   :58.77   Mean   :0.03386   Mean   :87.37  
    ##  3rd Qu.:0.00000   3rd Qu.:96.00   3rd Qu.:0.00000   3rd Qu.:96.00  
    ##  Max.   :1.00000   Max.   :96.00   Max.   :2.00000   Max.   :96.00  
    ##                    NA's   :2393                      NA's   :3087   
    ##    LSEXUSE3_I         LSEXUSE4       LSEXUSE4_I        meth12m1   
    ##  Min.   :0.00000   Min.   : 3.00   Min.   :0.0000   Min.   : 1.0  
    ##  1st Qu.:0.00000   1st Qu.:96.00   1st Qu.:0.0000   1st Qu.: 1.0  
    ##  Median :0.00000   Median :96.00   Median :0.0000   Median : 5.0  
    ##  Mean   :0.03386   Mean   :94.15   Mean   :0.0334   Mean   :37.2  
    ##  3rd Qu.:0.00000   3rd Qu.:96.00   3rd Qu.:0.0000   3rd Qu.:96.0  
    ##  Max.   :2.00000   Max.   :96.00   Max.   :1.0000   Max.   :96.0  
    ##                    NA's   :3183                     NA's   :1623  
    ##     meth12m2        meth12m3        meth12m4       meth3m1         meth3m2     
    ##  Min.   : 1.00   Min.   : 1.00   Min.   : 3.0   Min.   : 1.00   Min.   : 1.00  
    ##  1st Qu.: 6.00   1st Qu.:96.00   1st Qu.:96.0   1st Qu.: 2.00   1st Qu.: 8.00  
    ##  Median :96.00   Median :96.00   Median :96.0   Median : 7.00   Median :96.00  
    ##  Mean   :61.97   Mean   :88.81   Mean   :94.6   Mean   :38.51   Mean   :64.45  
    ##  3rd Qu.:96.00   3rd Qu.:96.00   3rd Qu.:96.0   3rd Qu.:96.00   3rd Qu.:96.00  
    ##  Max.   :96.00   Max.   :96.00   Max.   :96.0   Max.   :96.00   Max.   :96.00  
    ##  NA's   :2766    NA's   :3287    NA's   :3356   NA's   :2034    NA's   :3016   
    ##     meth3m3         meth3m4        PARTS1YR        PARTS1YR_I      
    ##  Min.   : 1.00   Min.   : 3.0   Min.   :0.0000   Min.   :0.000000  
    ##  1st Qu.:96.00   1st Qu.:96.0   1st Qu.:0.0000   1st Qu.:0.000000  
    ##  Median :96.00   Median :96.0   Median :1.0000   Median :0.000000  
    ##  Mean   :89.25   Mean   :94.7   Mean   :0.8598   Mean   :0.007321  
    ##  3rd Qu.:96.00   3rd Qu.:96.0   3rd Qu.:1.0000   3rd Qu.:0.000000  
    ##  Max.   :96.00   Max.   :96.0   Max.   :7.0000   Max.   :2.000000  
    ##  NA's   :3421    NA's   :3478                                      
    ##     PARTDUR1        PARTDUR2        PARTDUR3       PARTDUR1_I     
    ##  Min.   :  0.0   Min.   :  0.0   Min.   :  0.0   Min.   :0.00000  
    ##  1st Qu.: 16.0   1st Qu.:  4.0   1st Qu.:  6.0   1st Qu.:0.00000  
    ##  Median : 73.0   Median : 28.5   Median : 50.0   Median :0.00000  
    ##  Mean   :161.1   Mean   :346.6   Mean   :423.5   Mean   :0.03317  
    ##  3rd Qu.:169.0   3rd Qu.:997.0   3rd Qu.:997.0   3rd Qu.:0.00000  
    ##  Max.   :997.0   Max.   :997.0   Max.   :997.0   Max.   :2.00000  
    ##  NA's   :1009    NA's   :3941    NA's   :4134                     
    ##    PARTDUR2_I         PARTDUR3_I          NUMP3MOS        NUMP3MOS_I      
    ##  Min.   :0.000000   Min.   :0.000000   Min.   :0.0000   Min.   :0.000000  
    ##  1st Qu.:0.000000   1st Qu.:0.000000   1st Qu.:0.0000   1st Qu.:0.000000  
    ##  Median :0.000000   Median :0.000000   Median :1.0000   Median :0.000000  
    ##  Mean   :0.005948   Mean   :0.004576   Mean   :0.7659   Mean   :0.005948  
    ##  3rd Qu.:0.000000   3rd Qu.:0.000000   3rd Qu.:1.0000   3rd Qu.:0.000000  
    ##  Max.   :1.000000   Max.   :1.000000   Max.   :4.0000   Max.   :2.000000  
    ##                                        NA's   :1009                       
    ##     LIFPRTNR        LIFPRTNR_I          FMARNO          COHEVER     
    ##  Min.   : 0.000   Min.   :0.00000   Min.   :0.0000   Min.   :1.000  
    ##  1st Qu.: 1.000   1st Qu.:0.00000   1st Qu.:0.0000   1st Qu.:1.000  
    ##  Median : 3.000   Median :0.00000   Median :0.0000   Median :2.000  
    ##  Mean   : 7.526   Mean   :0.02013   Mean   :0.4194   Mean   :1.558  
    ##  3rd Qu.: 9.000   3rd Qu.:0.00000   3rd Qu.:1.0000   3rd Qu.:2.000  
    ##  Max.   :50.000   Max.   :2.00000   Max.   :6.0000   Max.   :2.000  
    ##                                                                     
    ##    COHEVER_I           evmarcoh        SEXONCE       SEXONCE_I        
    ##  Min.   :0.000000   Min.   :1.000   Min.   :1.00   Min.   :0.0000000  
    ##  1st Qu.:0.000000   1st Qu.:1.000   1st Qu.:2.00   1st Qu.:0.0000000  
    ##  Median :0.000000   Median :1.000   Median :2.00   Median :0.0000000  
    ##  Mean   :0.006406   Mean   :1.448   Mean   :1.98   Mean   :0.0006863  
    ##  3rd Qu.:0.000000   3rd Qu.:2.000   3rd Qu.:2.00   3rd Qu.:0.0000000  
    ##  Max.   :2.000000   Max.   :2.000   Max.   :2.00   Max.   :1.0000000  
    ##                                     NA's   :1009                      
    ##     VRY1STSX      VRY1STSX_I         vry1stag       FIRSTPFLAG   
    ##  Min.   :1035   Min.   :0.00000   Min.   :10.00   Min.   :1.000  
    ##  1st Qu.:1206   1st Qu.:0.00000   1st Qu.:16.00   1st Qu.:1.000  
    ##  Median :1298   Median :0.00000   Median :18.00   Median :1.000  
    ##  Mean   :1369   Mean   :0.02631   Mean   :18.61   Mean   :2.347  
    ##  3rd Qu.:1382   3rd Qu.:0.00000   3rd Qu.:20.00   3rd Qu.:1.000  
    ##  Max.   :9997   Max.   :2.00000   Max.   :46.00   Max.   :9.000  
    ##  NA's   :1009                     NA's   :1009    NA's   :1009   
    ##     FSEXRLTN       FSEXRLTN_I        SEX1MTHD1      SEX1MTHD1_I     
    ##  Min.   :1.000   Min.   :0.00000   Min.   : 1.00   Min.   :0.00000  
    ##  1st Qu.:5.000   1st Qu.:0.00000   1st Qu.: 1.00   1st Qu.:0.00000  
    ##  Median :6.000   Median :0.00000   Median : 1.00   Median :0.00000  
    ##  Mean   :5.801   Mean   :0.02883   Mean   :26.03   Mean   :0.03089  
    ##  3rd Qu.:7.000   3rd Qu.:0.00000   3rd Qu.:96.00   3rd Qu.:0.00000  
    ##  Max.   :9.000   Max.   :2.00000   Max.   :96.00   Max.   :1.00000  
    ##  NA's   :1009                      NA's   :1009                     
    ##    SEX1MTHD2      SEX1MTHD2_I        SEX1MTHD3      SEX1MTHD3_I     
    ##  Min.   : 1.00   Min.   :0.00000   Min.   : 1.00   Min.   :0.00000  
    ##  1st Qu.: 4.00   1st Qu.:0.00000   1st Qu.:96.00   1st Qu.:0.00000  
    ##  Median :96.00   Median :0.00000   Median :96.00   Median :0.00000  
    ##  Mean   :56.58   Mean   :0.03294   Mean   :86.57   Mean   :0.03157  
    ##  3rd Qu.:96.00   3rd Qu.:0.00000   3rd Qu.:96.00   3rd Qu.:0.00000  
    ##  Max.   :96.00   Max.   :2.00000   Max.   :96.00   Max.   :1.00000  
    ##  NA's   :2853                      NA's   :3399                     
    ##    SEX1MTHD4      SEX1MTHD4_I         MARDAT01      MARDAT01_I      
    ##  Min.   : 2.00   Min.   :0.00000   Min.   :1989   Min.   :0.000000  
    ##  1st Qu.:96.00   1st Qu.:0.00000   1st Qu.:2006   1st Qu.:0.000000  
    ##  Median :96.00   Median :0.00000   Median :2012   Median :0.000000  
    ##  Mean   :95.01   Mean   :0.03157   Mean   :2016   Mean   :0.006177  
    ##  3rd Qu.:96.00   3rd Qu.:0.00000   3rd Qu.:2017   3rd Qu.:0.000000  
    ##  Max.   :96.00   Max.   :1.00000   Max.   :9997   Max.   :2.000000  
    ##  NA's   :3490                      NA's   :2749                     
    ##     FMAR1AGE        MAREND01       MAREND01_I          MARDIS01   
    ##  Min.   :16.00   Min.   :1.000   Min.   :0.000000   Min.   :1994  
    ##  1st Qu.:23.25   1st Qu.:1.000   1st Qu.:0.000000   1st Qu.:2007  
    ##  Median :27.00   Median :1.000   Median :0.000000   Median :2013  
    ##  Mean   :27.23   Mean   :1.161   Mean   :0.001602   Mean   :2012  
    ##  3rd Qu.:30.00   3rd Qu.:1.000   3rd Qu.:0.000000   3rd Qu.:2018  
    ##  Max.   :48.00   Max.   :3.000   Max.   :1.000000   Max.   :2023  
    ##  NA's   :2749    NA's   :3955                       NA's   :3955  
    ##    MARDIS01_I          PREMARW1        mar1diss        COHAB1    
    ##  Min.   :0.000000   Min.   :1.000   Min.   :1.00   Min.   :1988  
    ##  1st Qu.:0.000000   1st Qu.:1.000   1st Qu.:4.00   1st Qu.:2005  
    ##  Median :0.000000   Median :1.000   Median :5.00   Median :2011  
    ##  Mean   :0.006635   Mean   :1.371   Mean   :4.22   Mean   :2011  
    ##  3rd Qu.:0.000000   3rd Qu.:2.000   3rd Qu.:5.00   3rd Qu.:2017  
    ##  Max.   :2.000000   Max.   :2.000   Max.   :5.00   Max.   :2023  
    ##                     NA's   :2750    NA's   :2749   NA's   :2440  
    ##     COHAB1_I          COHSTAT       COHSTAT_I          COHOUT     
    ##  Min.   :0.00000   Min.   :1.00   Min.   :0.0000   Min.   :1.000  
    ##  1st Qu.:0.00000   1st Qu.:1.00   1st Qu.:0.0000   1st Qu.:2.000  
    ##  Median :0.00000   Median :1.00   Median :0.0000   Median :3.000  
    ##  Mean   :0.02402   Mean   :1.46   Mean   :0.0119   Mean   :2.882  
    ##  3rd Qu.:0.00000   3rd Qu.:2.00   3rd Qu.:0.0000   3rd Qu.:4.000  
    ##  Max.   :2.00000   Max.   :3.00   Max.   :2.0000   Max.   :4.000  
    ##                                                    NA's   :2518   
    ##     COH1DUR        COH1DUR_I           sexmar         sexunion    
    ##  Min.   :1.000   Min.   :0.00000   Min.   :1.000   Min.   :1.000  
    ##  1st Qu.:1.000   1st Qu.:0.00000   1st Qu.:4.000   1st Qu.:3.000  
    ##  Median :2.000   Median :0.00000   Median :4.000   Median :4.000  
    ##  Mean   :2.672   Mean   :0.02677   Mean   :3.587   Mean   :3.369  
    ##  3rd Qu.:4.000   3rd Qu.:0.00000   3rd Qu.:4.000   3rd Qu.:4.000  
    ##  Max.   :5.000   Max.   :2.00000   Max.   :5.000   Max.   :5.000  
    ##  NA's   :2519                      NA's   :1009    NA's   :1009   
    ##     CSPBIOKD        CSPBIOKD_I    DATBABY1      DATBABY1_I      
    ##  Min.   : 0.000   Min.   :0    Min.   :1987   Min.   :0.000000  
    ##  1st Qu.: 0.000   1st Qu.:0    1st Qu.:2007   1st Qu.:0.000000  
    ##  Median : 1.000   Median :0    Median :2012   Median :0.000000  
    ##  Mean   : 1.093   Mean   :0    Mean   :2022   Mean   :0.002517  
    ##  3rd Qu.: 2.000   3rd Qu.:0    3rd Qu.:2017   3rd Qu.:0.000000  
    ##  Max.   :10.000   Max.   :0    Max.   :9997   Max.   :1.000000  
    ##  NA's   :2634                  NA's   :2921                     
    ##     agebaby1        b1premar        MARBABY1       MARBABY1_I     
    ##  Min.   :11.00   Min.   :1.000   Min.   :1.000   Min.   :0.00000  
    ##  1st Qu.:22.00   1st Qu.:1.000   1st Qu.:1.000   1st Qu.:0.00000  
    ##  Median :27.00   Median :2.000   Median :1.000   Median :0.00000  
    ##  Mean   :27.31   Mean   :1.616   Mean   :1.516   Mean   :0.05079  
    ##  3rd Qu.:32.00   3rd Qu.:2.000   3rd Qu.:2.000   3rd Qu.:0.00000  
    ##  Max.   :97.00   Max.   :2.000   Max.   :3.000   Max.   :2.00000  
    ##  NA's   :2921    NA's   :2921    NA's   :2921                     
    ##     COMPREG          COMPREG_I     WANTB1         WANTB1_I          DADTYPE    
    ##  Min.   : 0.0000   Min.   :0   Min.   :1.000   Min.   :0.00000   Min.   :1.00  
    ##  1st Qu.: 0.0000   1st Qu.:0   1st Qu.:2.000   1st Qu.:0.00000   1st Qu.:2.00  
    ##  Median : 0.0000   Median :0   Median :2.000   Median :0.00000   Median :4.00  
    ##  Mean   : 0.9218   Mean   :0   Mean   :2.214   Mean   :0.02791   Mean   :3.15  
    ##  3rd Qu.: 2.0000   3rd Qu.:0   3rd Qu.:2.000   3rd Qu.:0.00000   3rd Qu.:4.00  
    ##  Max.   :10.0000   Max.   :0   Max.   :7.000   Max.   :1.00000   Max.   :4.00  
    ##                                NA's   :4021                                    
    ##    DADTYPE_I     INTENT          ADDEXP       ADDEXP_I          CURR_INS    
    ##  Min.   :0   Min.   :1.000   Min.   :  0   Min.   :0.00000   Min.   :1.000  
    ##  1st Qu.:0   1st Qu.:1.000   1st Qu.:  0   1st Qu.:0.00000   1st Qu.:1.000  
    ##  Median :0   Median :2.000   Median :  0   Median :0.00000   Median :1.000  
    ##  Mean   :0   Mean   :1.564   Mean   : 10   Mean   :0.01235   Mean   :1.714  
    ##  3rd Qu.:0   3rd Qu.:2.000   3rd Qu.: 20   3rd Qu.:0.00000   3rd Qu.:2.000  
    ##  Max.   :0   Max.   :4.000   Max.   :330   Max.   :2.00000   Max.   :4.000  
    ##                                                                             
    ##    CURR_INS_I         EVHIVTST       RELIGION       RELIGION_I     
    ##  Min.   :0.00000   Min.   :0.00   Min.   :1.000   Min.   :0.00000  
    ##  1st Qu.:0.00000   1st Qu.:0.00   1st Qu.:1.000   1st Qu.:0.00000  
    ##  Median :0.00000   Median :1.00   Median :2.000   Median :0.00000  
    ##  Mean   :0.02928   Mean   :1.04   Mean   :2.139   Mean   :0.02334  
    ##  3rd Qu.:0.00000   3rd Qu.:2.00   3rd Qu.:3.000   3rd Qu.:0.00000  
    ##  Max.   :1.00000   Max.   :3.00   Max.   :4.000   Max.   :1.00000  
    ##                    NA's   :74                                      
    ##     LABORFOR       LABORFOR_I        TOTINCR        TOTINCR_I     
    ##  Min.   :1.000   Min.   :0.0000   Min.   : 1.00   Min.   :0.0000  
    ##  1st Qu.:1.000   1st Qu.:0.0000   1st Qu.:10.00   1st Qu.:0.0000  
    ##  Median :1.000   Median :0.0000   Median :13.00   Median :0.0000  
    ##  Mean   :2.332   Mean   :0.0151   Mean   :11.79   Mean   :0.1263  
    ##  3rd Qu.:4.000   3rd Qu.:0.0000   3rd Qu.:15.00   3rd Qu.:0.0000  
    ##  Max.   :7.000   Max.   :2.0000   Max.   :15.00   Max.   :2.0000  
    ##                                                                   
    ##     POVERTY        POVERTY_I          METRO        WGT2022_2023  
    ##  Min.   : 50.0   Min.   :0.0000   Min.   :1.000   Min.   : 1515  
    ##  1st Qu.:178.0   1st Qu.:0.0000   1st Qu.:1.000   1st Qu.: 7234  
    ##  Median :343.0   Median :0.0000   Median :2.000   Median :12744  
    ##  Mean   :351.2   Mean   :0.1263   Mean   :1.769   Mean   :17319  
    ##  3rd Qu.:537.0   3rd Qu.:0.0000   3rd Qu.:2.000   3rd Qu.:22706  
    ##  Max.   :700.0   Max.   :2.0000   Max.   :3.000   Max.   :95540  
    ##                                                                  
    ##       VEST            VECL         CMINTVW        CMLSTYR        CMFIVYR    
    ##  Min.   : 1.00   Min.   :1.00   Min.   :1465   Min.   :1453   Min.   :1405  
    ##  1st Qu.: 6.00   1st Qu.:1.00   1st Qu.:1474   1st Qu.:1462   1st Qu.:1414  
    ##  Median :11.00   Median :2.00   Median :1480   Median :1468   Median :1420  
    ##  Mean   :10.69   Mean   :2.46   Mean   :1478   Mean   :1466   Mean   :1418  
    ##  3rd Qu.:16.00   3rd Qu.:3.00   3rd Qu.:1483   3rd Qu.:1471   3rd Qu.:1423  
    ##  Max.   :20.00   Max.   :4.00   Max.   :1488   Max.   :1476   Max.   :1428  
    ##                                                                             
    ##       YEAR          QUARTER          PHASE1      PHASE2           PHASE3      
    ##  Min.   :1.000   Min.   :1.000   Min.   :1   Min.   :0.0000   Min.   :0.0000  
    ##  1st Qu.:1.000   1st Qu.:2.000   1st Qu.:1   1st Qu.:0.0000   1st Qu.:0.0000  
    ##  Median :2.000   Median :3.000   Median :1   Median :1.0000   Median :0.0000  
    ##  Mean   :1.667   Mean   :2.612   Mean   :1   Mean   :0.5104   Mean   :0.1437  
    ##  3rd Qu.:2.000   3rd Qu.:4.000   3rd Qu.:1   3rd Qu.:1.0000   3rd Qu.:0.0000  
    ##  Max.   :2.000   Max.   :4.000   Max.   :1   Max.   :1.0000   Max.   :1.0000  
    ## 

``` r
# missing values for numerical variables 
maleresp$RSCRAGE[is.na(maleresp$RSCRAGE)] <- mean(maleresp$RSCRAGE, na.rm = TRUE)

# missing values for categorical variables
maleresp$HISP[is.na(maleresp$HISP)] <- "Non-Hispanic"

#recoding categorical variables
maleresp$HISP <- as.factor(maleresp$HISP)
maleresp$RSCRRACE <- as.factor(maleresp$RSCRRACE)
maleresp$FTFMODE <- as.factor(maleresp$FTFMODE)

#creating derived variables
maleresp$AGE_CATEGORY <- cut(maleresp$RSCRAGE, 
                             breaks = c(15, 25, 35, 45, 50), 
                             labels = c("15-24", "25-34", "35-44", "45-49"), 
                             right = FALSE)
table(maleresp$AGE_CATEGORY)
```

    ## 
    ## 15-24 25-34 35-44 45-49 
    ##  1166  1377  1374   454

``` r
#statistical analysis
#poisson regression 
# Poisson regression model (e.g., number of household members as the count outcome)
poisson_model <- glm(ROSCNT ~ RSCRAGE + RSCRRACE + HISP + FTFMODE, 
                     family = poisson(link = "log"), 
                     data = maleresp)
```

``` r
#model summary (poisson)
summary(poisson_model)
```

    ## 
    ## Call:
    ## glm(formula = ROSCNT ~ RSCRAGE + RSCRRACE + HISP + FTFMODE, family = poisson(link = "log"), 
    ##     data = maleresp)
    ## 
    ## Coefficients:
    ##               Estimate Std. Error z value Pr(>|z|)    
    ## (Intercept)  1.4594465  0.0767986  19.004   <2e-16 ***
    ## RSCRAGE     -0.0087886  0.0009272  -9.479   <2e-16 ***
    ## RSCRRACE2   -0.0740530  0.0361087  -2.051   0.0403 *  
    ## RSCRRACE3   -0.0413868  0.0290349  -1.425   0.1540    
    ## RSCRRACE4   -0.0118112  0.0719731  -0.164   0.8696    
    ## HISP5       -0.1106936  0.0660828  -1.675   0.0939 .  
    ## HISP8       -1.0675625  0.7103427  -1.503   0.1329    
    ## HISP9        0.0883179  0.2161080   0.409   0.6828    
    ## FTFMODE2     0.0128601  0.0205363   0.626   0.5312    
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## (Dispersion parameter for poisson family taken to be 1)
    ## 
    ##     Null deviance: 3417.6  on 4370  degrees of freedom
    ## Residual deviance: 3263.5  on 4362  degrees of freedom
    ## AIC: 15686
    ## 
    ## Number of Fisher Scoring iterations: 4

``` r
#check the mean and variance 
# Check the mean and variance to detect overdispersion
mean_count <- mean(maleresp$ROSCNT)
var_count <- var(maleresp$ROSCNT)
cat("Mean:", mean_count, "\n")
```

    ## Mean: 2.920156

``` r
cat("Variance:", var_count, "\n")
```

    ## Variance: 2.293166

``` r
deviance_value <- deviance(poisson_model)
residual_degrees_of_freedom <- df.residual(poisson_model)

cat("Deviance: ", deviance_value, "\n")
```

    ## Deviance:  3263.502

``` r
cat("Residual Degrees of Freedom: ", residual_degrees_of_freedom, "\n")
```

    ## Residual Degrees of Freedom:  4362

``` r
# Check for missing values and handle them
sum(is.na(maleresp$HISP))
```

    ## [1] 0

``` r
sum(is.na(maleresp$RSCRRACE))
```

    ## [1] 0

``` r
# Remove rows with NA values
maleresp <- maleresp[!is.na(maleresp$HISP) & !is.na(maleresp$RSCRRACE), ]

# Convert to factors
maleresp$HISP <- as.factor(maleresp$HISP)
maleresp$RSCRRACE <- as.factor(maleresp$RSCRRACE)

# Create contingency table
contingency_table <- table(maleresp$HISP, maleresp$RSCRRACE)

# Perform Chi-square test
chi_square_result <- chisq.test(contingency_table)
```

    ## Warning in chisq.test(contingency_table): Chi-squared approximation may be
    ## incorrect

``` r
print(chi_square_result)
```

    ## 
    ##  Pearson's Chi-squared test
    ## 
    ## data:  contingency_table
    ## X-squared = 3925, df = 9, p-value < 2.2e-16

``` r
# If Chi-square is problematic, use Fisher's Exact Test with simulation
fisher_test_result <- fisher.test(contingency_table, simulate.p.value = TRUE)
print(fisher_test_result)
```

    ## 
    ##  Fisher's Exact Test for Count Data with simulated p-value (based on
    ##  2000 replicates)
    ## 
    ## data:  contingency_table
    ## p-value = 0.0004998
    ## alternative hypothesis: two.sided

``` r
# Check expected counts
expected_counts <- chisq.test(contingency_table)$expected
```

    ## Warning in chisq.test(contingency_table): Chi-squared approximation may be
    ## incorrect

``` r
print(expected_counts)
```

    ##    
    ##               1           2           3           4
    ##   1  97.3543811 121.8924731  489.963853 162.7892931
    ##   5 389.7524594 487.9892473 1961.541066 651.7172272
    ##   8   0.2232899   0.2795699    1.123770   0.3733699
    ##   9   0.6698696   0.8387097    3.371311   1.1201098

``` r
# Visualize with a mosaic plot
library(ggplot2)

ggplot(data = maleresp, aes(x = HISP, fill = RSCRRACE)) + 
  geom_bar(position = "dodge") + 
  labs(title = "Bar Plot: Hispanic Origin vs Race", 
       x = "Hispanic Origin (HISP)", 
       y = "Count of Individuals") + 
  theme_minimal()
```

![](QUINTERO_GONZALES_EDA_SA2_files/figure-gfm/unnamed-chunk-7-1.png)<!-- -->

``` r
library(MASS)
```

    ## Warning: package 'MASS' was built under R version 4.4.3

``` r
#ordinal logistic regression
maleresp$WHENSICK <- factor(maleresp$WHENSICK, 
                            ordered = TRUE)

ordinal_logit_model <- polr(WHENSICK ~ RSCRAGE + RSCRRACE + HISP + FTFMODE, 
                            data = maleresp, 
                            method = "logistic")

summary(ordinal_logit_model)
```

    ## 
    ## Re-fitting to get Hessian

    ## Call:
    ## polr(formula = WHENSICK ~ RSCRAGE + RSCRRACE + HISP + FTFMODE, 
    ##     data = maleresp, method = "logistic")
    ## 
    ## Coefficients:
    ##               Value Std. Error t value
    ## RSCRAGE   -0.004408    0.00287 -1.5360
    ## RSCRRACE2  0.242424    0.11198  2.1648
    ## RSCRRACE3 -0.051388    0.09077 -0.5661
    ## RSCRRACE4 -0.318288    0.23959 -1.3285
    ## HISP5     -0.113748    0.22085 -0.5150
    ## HISP8      3.594263    1.70661  2.1061
    ## HISP9      0.690203    0.80116  0.8615
    ## FTFMODE2   0.484821    0.06409  7.5651
    ## 
    ## Intercepts:
    ##     Value    Std. Error t value 
    ## 1|2  -2.6463   0.2590   -10.2188
    ## 2|3  -1.1672   0.2541    -4.5942
    ## 3|4   0.6637   0.2536     2.6168
    ## 4|5   2.0033   0.2557     7.8339
    ## 5|8   4.5443   0.2884    15.7579
    ## 8|9   5.2274   0.3195    16.3600
    ## 
    ## Residual Deviance: 12907.52 
    ## AIC: 12935.52

``` r
#multinomial logistic regression
library(nnet)

# Ensure PXMETHOD01 is a factor
maleresp$PXMETHOD01 <- as.factor(maleresp$PXMETHOD01)

# Multinomial logistic regression model
multinomial_logit_model <- multinom(PXMETHOD01 ~ RSCRAGE + RSCRRACE + HISP + FTFMODE, 
                                    data = maleresp)
```

    ## # weights:  140 (117 variable)
    ## initial  value 2230.003444 
    ## iter  10 value 1242.957043
    ## iter  20 value 1081.913352
    ## iter  30 value 1005.948905
    ## iter  40 value 997.993342
    ## iter  50 value 995.716128
    ## iter  60 value 994.986898
    ## iter  70 value 994.773416
    ## iter  80 value 994.706754
    ## iter  90 value 994.695780
    ## iter 100 value 994.693929
    ## final  value 994.693929 
    ## stopped after 100 iterations

``` r
summary(multinomial_logit_model)
```

    ## Warning in sqrt(diag(vc)): NaNs produced

    ## Call:
    ## multinom(formula = PXMETHOD01 ~ RSCRAGE + RSCRRACE + HISP + FTFMODE, 
    ##     data = maleresp)
    ## 
    ## Coefficients:
    ##    (Intercept)      RSCRAGE    RSCRRACE2  RSCRRACE3   RSCRRACE4       HISP5
    ## 2   -1.3851744  0.000861853  -0.48881982  0.1725292  -0.3504160 -0.08165290
    ## 3  -25.8899259  0.148859210  17.64722161 19.6346688  16.1150612 -2.24460673
    ## 4   -3.1825360  0.013706646  -0.67184472  0.1895634   0.7543031  0.69176842
    ## 5  -33.8557416  0.183429784  22.07098211 23.2462446  23.9695666  0.87495182
    ## 6  -20.3363928 -0.008886310  -0.04032707 16.2453200  16.6308006  0.05036908
    ## 7  -20.2527858 -0.028207651  16.11892712 17.1862632  17.5041220  0.17060798
    ## 8  -44.7160970  0.065534517  18.22175776 18.2376078  20.1201168  0.98439324
    ## 9  -20.8029568 -0.008221236 -10.78077199 -1.1357285   0.3263576  0.94327761
    ## 10 -19.2099007 -0.011554469   0.11917628 14.1372805  15.2603055 -0.48598199
    ## 11  -2.2885228  0.035838722  -1.24251950  0.2787515  -1.3094600 -1.12679948
    ## 12  -5.4500292  0.097062810   0.17871391  0.4621536 -14.0765041 -1.87481940
    ## 98   0.3126793 -0.030648500 -13.70777717 -1.8761644  -3.9381310 -2.01570019
    ## 99 -20.6733129  0.054301809  -4.73553375 14.8539169  15.0648050 -0.07721175
    ##    HISP8        HISP9      FTFMODE2
    ## 2      0 -15.28647503  -0.619340380
    ## 3      0  -7.62846445   0.121923322
    ## 4      0  -9.62264189  -0.003221242
    ## 5      0  -2.21197795  -0.293928703
    ## 6      0  -0.08496016  -0.235432022
    ## 7      0  -5.47710644  -0.374159291
    ## 8      0  -0.34334239  19.255817377
    ## 9      0   0.04807127  16.641695073
    ## 10     0  -0.17066001   0.394920442
    ## 11     0 -13.11001648  -0.153227273
    ## 12     0 -13.00402726  -0.223502885
    ## 98     0  -0.93035671  -0.780806699
    ## 99     0  -0.64697224 -11.141066667
    ## 
    ## Std. Errors:
    ##    (Intercept)    RSCRAGE    RSCRRACE2 RSCRRACE3    RSCRRACE4     HISP5
    ## 2     1.018997 0.01331162 4.695520e-01 0.4163619 9.483580e-01 0.8803120
    ## 3     1.336172 0.03906292 1.017858e+00 0.8087628 1.073763e+00 1.2163314
    ## 4     1.279103 0.01465987 5.562311e-01 0.4671059 1.168901e+00 1.1094379
    ## 5     2.161422 0.04179823 1.777986e+00 1.7276776 1.691869e+00 3.2558802
    ## 6     1.654977 0.05380157 7.957743e-06 2.5258676 1.341398e+00 3.6768767
    ## 7     1.672300 0.04191635 1.589317e+00 1.4610931 1.417519e+00 2.7352536
    ## 8     1.530054 0.04540110 2.099420e+00 2.0805227 2.641763e+00 4.6253042
    ## 9     2.299243 0.06264817 2.325363e-04 1.2427580 4.047691e+00 3.9938458
    ## 10    2.213302 0.07142038 5.160906e-05 3.4094416 1.779789e+00 4.9536108
    ## 11    1.047317 0.01697295 7.020513e-01 0.5181662 9.288687e-01 0.8137449
    ## 12    2.092100 0.03887277 1.222556e+00 1.1446051 4.370035e-05 1.1746213
    ## 98    1.850237 0.05152095 8.571530e-06 0.9569476 1.545980e+00 1.2536808
    ## 99    2.450680 0.07723665 5.788913e-07 3.5226779 1.876625e+00 5.0706698
    ##           HISP8        HISP9     FTFMODE2
    ## 2           NaN 1.231034e-07 2.408963e-01
    ## 3           NaN 4.491728e-05 6.428576e-01
    ## 4  4.870579e-14 1.143462e-05 2.786672e-01
    ## 5           NaN 1.041555e-02 5.848573e-01
    ## 6           NaN 2.733051e-08 9.567689e-01
    ## 7  1.082716e-14 1.289769e-03 7.089923e-01
    ## 8           NaN 1.746558e-09 1.530055e+00
    ## 9  1.105177e-15 1.113849e-12 2.299254e+00
    ## 10 1.828753e-24 2.049123e-07 1.267873e+00
    ## 11          NaN 4.698105e-07 3.270156e-01
    ## 12          NaN 9.137040e-07 6.849695e-01
    ## 98 0.000000e+00 1.521415e-06 8.602733e-01
    ## 99 0.000000e+00 1.422023e-09 9.689243e-05
    ## 
    ## Residual Deviance: 1989.388 
    ## AIC: 2197.388

``` r
#EDA
# Histogram for age distribution
hist(maleresp$RSCRAGE, breaks = 10, main = "Age Distribution", xlab = "Age", col = "lightblue")
```

![](QUINTERO_GONZALES_EDA_SA2_files/figure-gfm/unnamed-chunk-10-1.png)<!-- -->

``` r
# Assuming RSCRRACE is coded as 1=White, 2=Black, 3=Hispanic, 4=Other
maleresp$RaceLabel <- factor(maleresp$RSCRRACE,
                             levels = c(1, 2, 3, 4),
                             labels = c("White", "Black", "Hispanic", "Other"))

boxplot(ROSCNT ~ RaceLabel,
        data = maleresp,
        main = "Household Size by Race",
        xlab = "Race",
        ylab = "Household Size",
        col = "lightblue")
```

![](QUINTERO_GONZALES_EDA_SA2_files/figure-gfm/unnamed-chunk-10-2.png)<!-- -->

``` r
# Bar chart for interview mode distribution
barplot(table(maleresp$FTFMODE), main = "Interview Mode Distribution", col = "lightgreen")
```

![](QUINTERO_GONZALES_EDA_SA2_files/figure-gfm/unnamed-chunk-10-3.png)<!-- -->

``` r
#multiple test
# Example p-values from multiple tests
p_values <- c(0.001, 0.05, 0.01)

# Adjust p-values using Bonferroni correction
adjusted_p_values_bonf <- p.adjust(p_values, method = "bonferroni")
cat("Adjusted p-values (Bonferroni):", adjusted_p_values_bonf, "\n")
```

    ## Adjusted p-values (Bonferroni): 0.003 0.15 0.03

``` r
# Adjust p-values using FDR method
adjusted_p_values_fdr <- p.adjust(p_values, method = "fdr")
cat("Adjusted p-values (FDR):", adjusted_p_values_fdr, "\n")
```

    ## Adjusted p-values (FDR): 0.003 0.05 0.015

``` r
# ANOVA on household size by race
anova_model <- aov(ROSCNT ~ RaceLabel, data = maleresp)
summary(anova_model)
```

    ##               Df Sum Sq Mean Sq F value   Pr(>F)    
    ## RaceLabel      3    169   56.49   25.04 4.66e-16 ***
    ## Residuals   4367   9852    2.26                     
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1

``` r
# Tukey HSD post-hoc test
tukey_results <- TukeyHSD(anova_model)
print(tukey_results)
```

    ##   Tukey multiple comparisons of means
    ##     95% family-wise confidence level
    ## 
    ## Fit: aov(formula = ROSCNT ~ RaceLabel, data = maleresp)
    ## 
    ## $RaceLabel
    ##                       diff        lwr        upr     p adj
    ## Black-White    -0.16929382 -0.4036456 0.06505800 0.2471660
    ## Hispanic-White -0.11767768 -0.3089908 0.07363546 0.3896842
    ## Other-White     0.38255384  0.1616599 0.60344779 0.0000518
    ## Hispanic-Black  0.05161614 -0.1228946 0.22612686 0.8723242
    ## Other-Black     0.55184766  0.3453352 0.75836015 0.0000000
    ## Other-Hispanic  0.50023153  0.3442593 0.65620380 0.0000000

``` r
# Plot Tukey HSD results
plot(tukey_results, las = 1)
```

![](QUINTERO_GONZALES_EDA_SA2_files/figure-gfm/unnamed-chunk-12-1.png)<!-- -->

Note that the `echo = FALSE` parameter was added to the code chunk to
prevent printing of the R code that generated the plot.
