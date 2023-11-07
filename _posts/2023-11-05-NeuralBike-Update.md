---
navigation: true
cover: 'assets/images/mainUnit1.jpg'
title: NeuralBike Update
date: 2023-11-05
class: post-template
---

Today I finally found the time to finish the pcb of the main controller for the Crash detection project. I have been working on this in the background for the past few weeks and it's finally complete today! 

The design is somewhat simple. On the top there's the Particle Boron LTE (which will be running inference) and there's also the MPU6050 (the IMU used to collect acceleromter data). But we also need to store that data so on the bottom there's a SD Card Module. This module runs on 5 volts but the Particle Boron runs on 3.3 volts, so to make them compatible, I shorted the input and the output of the voltage converter on the module so that it can run on 3.3 volts. 

Here is a picture if you want to see how the final product turned out:

![The main pcb](assets/images/mainUnit2.jpg)

Now I need a good case to put this in. I finally ended up with this design:

```stl
solid Mesh
  facet normal 0.000000 -0.052334 0.998630
    outer loop
      vertex 22.250000 -2.000000 -6.000000
      vertex 9.250000 -2.000000 -6.000000
      vertex 9.244522 -2.104528 -6.005478
    endloop
  endfacet
  facet normal 0.000000 -0.052334 0.998630
    outer loop
      vertex 22.250000 -2.000000 -6.000000
      vertex 9.244522 -2.104528 -6.005478
      vertex 22.255478 -2.104528 -6.005478
    endloop
  endfacet
  facet normal 0.000000 -0.156437 0.987688
    outer loop
      vertex 22.271852 -2.207912 -6.021852
      vertex 22.255478 -2.104528 -6.005478
      vertex 9.244522 -2.104528 -6.005478
    endloop
  endfacet
  facet normal 0.000000 -0.156437 0.987688
    outer loop
      vertex 22.271852 -2.207912 -6.021852
      vertex 9.244522 -2.104528 -6.005478
      vertex 9.228148 -2.207912 -6.021852
    endloop
  endfacet
  facet normal 0.000000 -0.258819 0.965926
    outer loop
      vertex 22.298943 -2.309017 -6.048944
      vertex 22.271852 -2.207912 -6.021852
      vertex 9.228148 -2.207912 -6.021852
    endloop
  endfacet
  facet normal 0.000000 -0.258819 0.965926
    outer loop
      vertex 22.298943 -2.309017 -6.048944
      vertex 9.228148 -2.207912 -6.021852
      vertex 9.201056 -2.309017 -6.048944
    endloop
  endfacet
  facet normal 0.000000 -0.358370 0.933580
    outer loop
      vertex 22.336454 -2.406737 -6.086455
      vertex 22.298943 -2.309017 -6.048944
      vertex 9.201056 -2.309017 -6.048944
    endloop
  endfacet
  facet normal 0.000000 -0.358370 0.933580
    outer loop
      vertex 22.336454 -2.406737 -6.086455
      vertex 9.201056 -2.309017 -6.048944
      vertex 9.163546 -2.406737 -6.086455
    endloop
  endfacet
  facet normal 0.000000 -0.453988 0.891008
    outer loop
      vertex 22.383974 -2.500000 -6.133975
      vertex 22.336454 -2.406737 -6.086455
      vertex 9.163546 -2.406737 -6.086455
    endloop
  endfacet
  facet normal 0.000000 -0.453988 0.891008
    outer loop
      vertex 22.383974 -2.500000 -6.133975
      vertex 9.163546 -2.406737 -6.086455
      vertex 9.116026 -2.500000 -6.133975
    endloop
  endfacet
  facet normal 0.000000 -0.544641 0.838669
    outer loop
      vertex 22.440983 -2.587785 -6.190983
      vertex 22.383974 -2.500000 -6.133975
      vertex 9.116026 -2.500000 -6.133975
    endloop
  endfacet
  facet normal 0.000000 -0.544641 0.838669
    outer loop
      vertex 22.440983 -2.587785 -6.190983
      vertex 9.116026 -2.500000 -6.133975
      vertex 9.059016 -2.587785 -6.190983
    endloop
  endfacet
  facet normal 0.000000 -0.629317 0.777149
    outer loop
      vertex 22.506855 -2.669131 -6.256855
      vertex 22.440983 -2.587785 -6.190983
      vertex 9.059016 -2.587785 -6.190983
    endloop
  endfacet
  facet normal 0.000000 -0.629317 0.777149
    outer loop
      vertex 22.506855 -2.669131 -6.256855
      vertex 9.059016 -2.587785 -6.190983
      vertex 8.993145 -2.669131 -6.256855
    endloop
  endfacet
  facet normal 0.000000 -0.707110 0.707103
    outer loop
      vertex 22.580870 -2.743145 -6.330870
      vertex 22.506855 -2.669131 -6.256855
      vertex 8.993145 -2.669131 -6.256855
    endloop
  endfacet
  facet normal 0.000000 -0.707110 0.707103
    outer loop
      vertex 22.580870 -2.743145 -6.330870
      vertex 8.993145 -2.669131 -6.256855
      vertex 8.919131 -2.743145 -6.330870
    endloop
  endfacet
  facet normal 0.000000 -0.777145 0.629322
    outer loop
      vertex 22.662214 -2.809017 -6.412215
      vertex 22.580870 -2.743145 -6.330870
      vertex 8.919131 -2.743145 -6.330870
    endloop
  endfacet
  facet normal 0.000000 -0.777145 0.629322
    outer loop
      vertex 22.662214 -2.809017 -6.412215
      vertex 8.919131 -2.743145 -6.330870
      vertex 8.837786 -2.809017 -6.412215
    endloop
  endfacet
  facet normal 0.000000 -0.838671 0.544638
    outer loop
      vertex 22.750000 -2.866025 -6.500000
      vertex 22.662214 -2.809017 -6.412215
      vertex 8.837786 -2.809017 -6.412215
    endloop
  endfacet
  facet normal 0.000000 -0.838671 0.544638
    outer loop
      vertex 22.750000 -2.866025 -6.500000
      vertex 8.837786 -2.809017 -6.412215
      vertex 8.750000 -2.866025 -6.500000
    endloop
  endfacet
  facet normal 0.000000 -0.891006 0.453992
    outer loop
      vertex 8.656736 -2.913545 -6.593263
      vertex 22.750000 -2.866025 -6.500000
      vertex 8.750000 -2.866025 -6.500000
    endloop
  endfacet
  facet normal 0.000000 -0.998630 0.052334
    outer loop
      vertex 8.354528 -2.994522 -6.895472
      vertex 8.250000 -3.000000 -7.000000
      vertex 23.250000 -3.000000 -7.000000
    endloop
  endfacet
  facet normal 0.000000 -0.998630 0.052334
    outer loop
      vertex 8.354528 -2.994522 -6.895472
      vertex 23.250000 -3.000000 -7.000000
      vertex 23.145472 -2.994522 -6.895472
    endloop
  endfacet
  facet normal 0.000000 -0.987688 0.156435
    outer loop
      vertex 8.457912 -2.978148 -6.792089
      vertex 8.354528 -2.994522 -6.895472
      vertex 23.145472 -2.994522 -6.895472
    endloop
  endfacet
  facet normal 0.000000 -0.987688 0.156435
    outer loop
      vertex 8.457912 -2.978148 -6.792089
      vertex 23.145472 -2.994522 -6.895472
      vertex 23.042088 -2.978148 -6.792089
    endloop
  endfacet
  facet normal 0.000000 -0.965925 0.258821
    outer loop
      vertex 8.559017 -2.951056 -6.690983
      vertex 8.457912 -2.978148 -6.792089
      vertex 23.042088 -2.978148 -6.792089
    endloop
  endfacet
  facet normal 0.000000 -0.965925 0.258821
    outer loop
      vertex 8.559017 -2.951056 -6.690983
      vertex 23.042088 -2.978148 -6.792089
      vertex 22.940983 -2.951056 -6.690983
    endloop
  endfacet
  facet normal 0.000000 -0.933581 0.358367
    outer loop
      vertex 8.656736 -2.913545 -6.593263
      vertex 8.559017 -2.951056 -6.690983
      vertex 22.940983 -2.951056 -6.690983
    endloop
  endfacet
  facet normal 0.000000 -0.933581 0.358367
    outer loop
      vertex 8.656736 -2.913545 -6.593263
      vertex 22.940983 -2.951056 -6.690983
      vertex 22.843264 -2.913545 -6.593263
    endloop
  endfacet
  facet normal 0.000000 -0.891006 0.453992
    outer loop
      vertex 22.750000 -2.866025 -6.500000
      vertex 8.656736 -2.913545 -6.593263
      vertex 22.843264 -2.913545 -6.593263
    endloop
  endfacet
  facet normal 0.000000 -0.998630 -0.052334
    outer loop
      vertex 23.145472 -2.994522 -3.604528
      vertex 23.250000 -3.000000 -3.500000
      vertex 8.250000 -3.000000 -3.500000
    endloop
  endfacet
  facet normal -0.000000 -0.998630 -0.052334
    outer loop
      vertex 23.145472 -2.994522 -3.604528
      vertex 8.250000 -3.000000 -3.500000
      vertex 8.354528 -2.994522 -3.604528
    endloop
  endfacet
  facet normal 0.000000 -0.987688 -0.156435
    outer loop
      vertex 23.042088 -2.978148 -3.707911
      vertex 23.145472 -2.994522 -3.604528
      vertex 8.354528 -2.994522 -3.604528
    endloop
  endfacet
  facet normal -0.000000 -0.987688 -0.156435
    outer loop
      vertex 23.042088 -2.978148 -3.707911
      vertex 8.354528 -2.994522 -3.604528
      vertex 8.457912 -2.978148 -3.707911
    endloop
  endfacet
  facet normal 0.000000 -0.965926 -0.258820
    outer loop
      vertex 22.940983 -2.951056 -3.809017
      vertex 23.042088 -2.978148 -3.707911
      vertex 8.457912 -2.978148 -3.707911
    endloop
  endfacet
  facet normal -0.000000 -0.965926 -0.258820
    outer loop
      vertex 22.940983 -2.951056 -3.809017
      vertex 8.457912 -2.978148 -3.707911
      vertex 8.559017 -2.951056 -3.809017
    endloop
  endfacet
  facet normal 0.000000 -0.933580 -0.358368
    outer loop
      vertex 22.843264 -2.913545 -3.906737
      vertex 22.940983 -2.951056 -3.809017
      vertex 8.559017 -2.951056 -3.809017
    endloop
  endfacet
  facet normal -0.000000 -0.933580 -0.358368
    outer loop
      vertex 22.843264 -2.913545 -3.906737
      vertex 8.559017 -2.951056 -3.809017
      vertex 8.656736 -2.913545 -3.906737
    endloop
  endfacet
  facet normal 0.000000 -0.891006 -0.453991
    outer loop
      vertex 22.750000 -2.866025 -4.000000
      vertex 22.843264 -2.913545 -3.906737
      vertex 8.656736 -2.913545 -3.906737
    endloop
  endfacet
  facet normal -0.000000 -0.891006 -0.453991
    outer loop
      vertex 22.750000 -2.866025 -4.000000
      vertex 8.656736 -2.913545 -3.906737
      vertex 8.750000 -2.866025 -4.000000
    endloop
  endfacet
  facet normal 0.000000 -0.838671 -0.544638
    outer loop
      vertex 22.662214 -2.809017 -4.087785
      vertex 22.750000 -2.866025 -4.000000
      vertex 8.750000 -2.866025 -4.000000
    endloop
  endfacet
  facet normal -0.000000 -0.838671 -0.544638
    outer loop
      vertex 22.662214 -2.809017 -4.087785
      vertex 8.750000 -2.866025 -4.000000
      vertex 8.837786 -2.809017 -4.087785
    endloop
  endfacet
  facet normal 0.000000 -0.777147 -0.629320
    outer loop
      vertex 22.580870 -2.743145 -4.169131
      vertex 22.662214 -2.809017 -4.087785
      vertex 8.837786 -2.809017 -4.087785
    endloop
  endfacet
  facet normal -0.000000 -0.777147 -0.629320
    outer loop
      vertex 22.580870 -2.743145 -4.169131
      vertex 8.837786 -2.809017 -4.087785
      vertex 8.919131 -2.743145 -4.169131
    endloop
  endfacet
  facet normal 0.000000 -0.707108 -0.707106
    outer loop
      vertex 22.506855 -2.669131 -4.243145
      vertex 22.580870 -2.743145 -4.169131
      vertex 8.919131 -2.743145 -4.169131
    endloop
  endfacet
  facet normal -0.000000 -0.707108 -0.707106
    outer loop
      vertex 22.506855 -2.669131 -4.243145
      vertex 8.919131 -2.743145 -4.169131
      vertex 8.993145 -2.669131 -4.243145
    endloop
  endfacet
  facet normal -0.000000 -0.629320 -0.777147
    outer loop
      vertex 22.506855 -2.669131 -4.243145
      vertex 8.993145 -2.669131 -4.243145
      vertex 9.059016 -2.587785 -4.309017
    endloop
  endfacet
  facet normal -0.000000 -0.629320 -0.777147
    outer loop
      vertex 22.440983 -2.587785 -4.309017
      vertex 22.506855 -2.669131 -4.243145
      vertex 9.059016 -2.587785 -4.309017
    endloop
  endfacet
  facet normal -0.000000 -0.544638 -0.838671
    outer loop
      vertex 22.440983 -2.587785 -4.309017
      vertex 9.059016 -2.587785 -4.309017
      vertex 22.383974 -2.500000 -4.366025
    endloop
  endfacet
  facet normal -0.000000 -0.544638 -0.838671
    outer loop
      vertex 22.383974 -2.500000 -4.366025
      vertex 9.059016 -2.587785 -4.309017
      vertex 9.116026 -2.500000 -4.366025
    endloop
  endfacet
  facet normal -0.000000 -0.453991 -0.891006
    outer loop
      vertex 22.383974 -2.500000 -4.366025
      vertex 9.116026 -2.500000 -4.366025
      vertex 9.163546 -2.406737 -4.413546
    endloop
  endfacet
  facet normal -0.000000 -0.453991 -0.891006
    outer loop
      vertex 22.336454 -2.406737 -4.413546
      vertex 22.383974 -2.500000 -4.366025
      vertex 9.163546 -2.406737 -4.413546
    endloop
  endfacet
  facet normal -0.000000 -0.358366 -0.933581
    outer loop
      vertex 22.336454 -2.406737 -4.413546
      vertex 9.163546 -2.406737 -4.413546
      vertex 22.298943 -2.309017 -4.451056
    endloop
  endfacet
  facet normal -0.000000 -0.358366 -0.933581
    outer loop
      vertex 22.298943 -2.309017 -4.451056
      vertex 9.163546 -2.406737 -4.413546
      vertex 9.201056 -2.309017 -4.451056
    endloop
  endfacet
  facet normal -0.000000 -0.258819 -0.965926
    outer loop
      vertex 22.298943 -2.309017 -4.451056
      vertex 9.201056 -2.309017 -4.451056
      vertex 9.228148 -2.207912 -4.478148
    endloop
  endfacet
  facet normal -0.000000 -0.258819 -0.965926
    outer loop
      vertex 22.271852 -2.207912 -4.478148
      vertex 22.298943 -2.309017 -4.451056
      vertex 9.228148 -2.207912 -4.478148
    endloop
  endfacet
  facet normal -0.000000 -0.156433 -0.987689
    outer loop
      vertex 22.271852 -2.207912 -4.478148
      vertex 9.228148 -2.207912 -4.478148
      vertex 22.255478 -2.104528 -4.494522
    endloop
  endfacet
  facet normal -0.000000 -0.156433 -0.987689
    outer loop
      vertex 22.255478 -2.104528 -4.494522
      vertex 9.228148 -2.207912 -4.478148
      vertex 9.244522 -2.104528 -4.494522
    endloop
  endfacet
  facet normal -0.000000 -0.052339 -0.998629
    outer loop
      vertex 22.255478 -2.104528 -4.494522
      vertex 9.244522 -2.104528 -4.494522
      vertex 9.250000 -2.000000 -4.500000
    endloop
  endfacet
  facet normal -0.000000 -0.052339 -0.998629
    outer loop
      vertex 22.250000 -2.000000 -4.500000
      vertex 22.255478 -2.104528 -4.494522
      vertex 9.250000 -2.000000 -4.500000
    endloop
  endfacet
  facet normal 0.998533 -0.054139 0.000000
    outer loop
      vertex 4.132328 1.135149 -4.500000
      vertex 4.125000 1.000000 -4.500000
      vertex 4.125000 1.000000 -6.500000
    endloop
  endfacet
  facet normal 0.998533 -0.054139 0.000000
    outer loop
      vertex 4.132328 1.135149 -4.500000
      vertex 4.125000 1.000000 -6.500000
      vertex 4.132328 1.135149 -6.500000
    endloop
  endfacet
  facet normal 0.986826 -0.161783 0.000000
    outer loop
      vertex 4.154224 1.268713 -4.500000
      vertex 4.132328 1.135149 -4.500000
      vertex 4.132328 1.135149 -6.500000
    endloop
  endfacet
  facet normal 0.986826 -0.161783 0.000000
    outer loop
      vertex 4.154224 1.268713 -4.500000
      vertex 4.132328 1.135149 -6.500000
      vertex 4.154224 1.268713 -6.500000
    endloop
  endfacet
  facet normal 0.963550 -0.267527 0.000000
    outer loop
      vertex 4.190434 1.399127 -4.500000
      vertex 4.154224 1.268713 -4.500000
      vertex 4.154224 1.268713 -6.500000
    endloop
  endfacet
  facet normal 0.963550 -0.267527 0.000000
    outer loop
      vertex 4.190434 1.399127 -4.500000
      vertex 4.154224 1.268713 -6.500000
      vertex 4.190434 1.399127 -6.500000
    endloop
  endfacet
  facet normal 0.928977 -0.370137 0.000000
    outer loop
      vertex 4.240530 1.524861 -4.500000
      vertex 4.190434 1.399127 -4.500000
      vertex 4.190434 1.399127 -6.500000
    endloop
  endfacet
  facet normal 0.928977 -0.370137 0.000000
    outer loop
      vertex 4.240530 1.524861 -4.500000
      vertex 4.190434 1.399127 -6.500000
      vertex 4.240530 1.524861 -6.500000
    endloop
  endfacet
  facet normal 0.883512 -0.468409 0.000000
    outer loop
      vertex 4.303928 1.644442 -4.500000
      vertex 4.240530 1.524861 -4.500000
      vertex 4.240530 1.524861 -6.500000
    endloop
  endfacet
  facet normal 0.883512 -0.468409 0.000000
    outer loop
      vertex 4.303928 1.644442 -4.500000
      vertex 4.240530 1.524861 -6.500000
      vertex 4.303928 1.644442 -6.500000
    endloop
  endfacet
  facet normal 0.827688 -0.561189 0.000000
    outer loop
      vertex 4.379884 1.756468 -4.500000
      vertex 4.303928 1.644442 -4.500000
      vertex 4.303928 1.644442 -6.500000
    endloop
  endfacet
  facet normal 0.827688 -0.561189 0.000000
    outer loop
      vertex 4.379884 1.756468 -4.500000
      vertex 4.303928 1.644442 -6.500000
      vertex 4.379884 1.756468 -6.500000
    endloop
  endfacet
  facet normal 0.762163 -0.647385 0.000000
    outer loop
      vertex 4.467505 1.859624 -4.500000
      vertex 4.379884 1.756468 -4.500000
      vertex 4.379884 1.756468 -6.500000
    endloop
  endfacet
  facet normal 0.762163 -0.647385 0.000000
    outer loop
      vertex 4.467505 1.859624 -4.500000
      vertex 4.379884 1.756468 -6.500000
      vertex 4.467505 1.859624 -6.500000
    endloop
  endfacet
  facet normal 0.687700 -0.725995 0.000000
    outer loop
      vertex 4.565767 1.952703 -4.500000
      vertex 4.467505 1.859624 -4.500000
      vertex 4.467505 1.859624 -6.500000
    endloop
  endfacet
  facet normal 0.687700 -0.725995 0.000000
    outer loop
      vertex 4.565767 1.952703 -4.500000
      vertex 4.467505 1.859624 -6.500000
      vertex 4.565767 1.952703 -6.500000
    endloop
  endfacet
  facet normal 0.605173 -0.796094 0.000000
    outer loop
      vertex 4.673516 2.034611 -4.500000
      vertex 4.565767 1.952703 -4.500000
      vertex 4.565767 1.952703 -6.500000
    endloop
  endfacet
  facet normal 0.605173 -0.796094 0.000000
    outer loop
      vertex 4.673516 2.034611 -4.500000
      vertex 4.565767 1.952703 -6.500000
      vertex 4.673516 2.034611 -6.500000
    endloop
  endfacet
  facet normal 0.515554 -0.856857 0.000000
    outer loop
      vertex 4.789489 2.104390 -4.500000
      vertex 4.673516 2.034611 -4.500000
      vertex 4.673516 2.034611 -6.500000
    endloop
  endfacet
  facet normal 0.515554 -0.856857 0.000000
    outer loop
      vertex 4.789489 2.104390 -4.500000
      vertex 4.673516 2.034611 -6.500000
      vertex 4.789489 2.104390 -6.500000
    endloop
  endfacet
  facet normal 0.419889 -0.907575 0.000000
    outer loop
      vertex 4.912327 2.161221 -4.500000
      vertex 4.789489 2.104390 -4.500000
      vertex 4.789489 2.104390 -6.500000
    endloop
  endfacet
  facet normal 0.419889 -0.907575 0.000000
    outer loop
      vertex 4.912327 2.161221 -4.500000
      vertex 4.789489 2.104390 -6.500000
      vertex 4.912327 2.161221 -6.500000
    endloop
  endfacet
  facet normal 0.319302 -0.947653 0.000000
    outer loop
      vertex 5.040590 2.204437 -4.500000
      vertex 4.912327 2.161221 -4.500000
      vertex 4.912327 2.161221 -6.500000
    endloop
  endfacet
  facet normal 0.319302 -0.947653 0.000000
    outer loop
      vertex 5.040590 2.204437 -4.500000
      vertex 4.912327 2.161221 -6.500000
      vertex 5.040590 2.204437 -6.500000
    endloop
  endfacet
  facet normal 0.214971 -0.976620 0.000000
    outer loop
      vertex 5.172772 2.233533 -4.500000
      vertex 5.040590 2.204437 -4.500000
      vertex 5.040590 2.204437 -6.500000
    endloop
  endfacet
  facet normal 0.214971 -0.976620 0.000000
    outer loop
      vertex 5.172772 2.233533 -4.500000
      vertex 5.040590 2.204437 -6.500000
      vertex 5.172772 2.233533 -6.500000
    endloop
  endfacet
  facet normal 0.108119 -0.994138 0.000000
    outer loop
      vertex 5.307327 2.248167 -4.500000
      vertex 5.172772 2.233533 -4.500000
      vertex 5.172772 2.233533 -6.500000
    endloop
  endfacet
  facet normal 0.108119 -0.994138 0.000000
    outer loop
      vertex 5.307327 2.248167 -4.500000
      vertex 5.172772 2.233533 -6.500000
      vertex 5.307327 2.248167 -6.500000
    endloop
  endfacet
  facet normal -0.000000 -1.000000 0.000000
    outer loop
      vertex 5.442674 2.248167 -4.500000
      vertex 5.307327 2.248167 -4.500000
      vertex 5.307327 2.248167 -6.500000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 -0.000000
    outer loop
      vertex 5.442674 2.248167 -4.500000
      vertex 5.307327 2.248167 -6.500000
      vertex 5.442674 2.248167 -6.500000
    endloop
  endfacet
  facet normal -0.108119 -0.994138 0.000000
    outer loop
      vertex 5.577228 2.233533 -4.500000
      vertex 5.442674 2.248167 -4.500000
      vertex 5.442674 2.248167 -6.500000
    endloop
  endfacet
  facet normal -0.108119 -0.994138 -0.000000
    outer loop
      vertex 5.577228 2.233533 -4.500000
      vertex 5.442674 2.248167 -6.500000
      vertex 5.577228 2.233533 -6.500000
    endloop
  endfacet
  facet normal -0.214970 -0.976621 0.000000
    outer loop
      vertex 5.709411 2.204437 -4.500000
      vertex 5.577228 2.233533 -4.500000
      vertex 5.577228 2.233533 -6.500000
    endloop
  endfacet
  facet normal -0.214970 -0.976621 -0.000000
    outer loop
      vertex 5.709411 2.204437 -4.500000
      vertex 5.577228 2.233533 -6.500000
      vertex 5.709411 2.204437 -6.500000
    endloop
  endfacet
  facet normal -0.319303 -0.947653 0.000000
    outer loop
      vertex 5.837673 2.161221 -4.500000
      vertex 5.709411 2.204437 -4.500000
      vertex 5.709411 2.204437 -6.500000
    endloop
  endfacet
  facet normal -0.319303 -0.947653 -0.000000
    outer loop
      vertex 5.837673 2.161221 -4.500000
      vertex 5.709411 2.204437 -6.500000
      vertex 5.837673 2.161221 -6.500000
    endloop
  endfacet
  facet normal -0.419889 -0.907575 0.000000
    outer loop
      vertex 5.960511 2.104390 -4.500000
      vertex 5.837673 2.161221 -4.500000
      vertex 5.837673 2.161221 -6.500000
    endloop
  endfacet
  facet normal -0.419889 -0.907575 -0.000000
    outer loop
      vertex 5.960511 2.104390 -4.500000
      vertex 5.837673 2.161221 -6.500000
      vertex 5.960511 2.104390 -6.500000
    endloop
  endfacet
  facet normal -0.515553 -0.856858 0.000000
    outer loop
      vertex 6.076484 2.034611 -4.500000
      vertex 5.960511 2.104390 -4.500000
      vertex 5.960511 2.104390 -6.500000
    endloop
  endfacet
  facet normal -0.515553 -0.856858 -0.000000
    outer loop
      vertex 6.076484 2.034611 -4.500000
      vertex 5.960511 2.104390 -6.500000
      vertex 6.076484 2.034611 -6.500000
    endloop
  endfacet
  facet normal -0.605176 -0.796092 0.000000
    outer loop
      vertex 6.184233 1.952703 -4.500000
      vertex 6.076484 2.034611 -4.500000
      vertex 6.076484 2.034611 -6.500000
    endloop
  endfacet
  facet normal -0.605176 -0.796092 -0.000000
    outer loop
      vertex 6.184233 1.952703 -4.500000
      vertex 6.076484 2.034611 -6.500000
      vertex 6.184233 1.952703 -6.500000
    endloop
  endfacet
  facet normal -0.687698 -0.725997 0.000000
    outer loop
      vertex 6.282495 1.859624 -4.500000
      vertex 6.184233 1.952703 -4.500000
      vertex 6.184233 1.952703 -6.500000
    endloop
  endfacet
  facet normal -0.687698 -0.725997 -0.000000
    outer loop
      vertex 6.282495 1.859624 -4.500000
      vertex 6.184233 1.952703 -6.500000
      vertex 6.282495 1.859624 -6.500000
    endloop
  endfacet
  facet normal -0.762161 -0.647387 0.000000
    outer loop
      vertex 6.370117 1.756468 -4.500000
      vertex 6.282495 1.859624 -4.500000
      vertex 6.282495 1.859624 -6.500000
    endloop
  endfacet
  facet normal -0.762161 -0.647387 -0.000000
    outer loop
      vertex 6.370117 1.756468 -4.500000
      vertex 6.282495 1.859624 -6.500000
      vertex 6.370117 1.756468 -6.500000
    endloop
  endfacet
  facet normal -0.827690 -0.561186 0.000000
    outer loop
      vertex 6.446072 1.644442 -4.500000
      vertex 6.370117 1.756468 -4.500000
      vertex 6.370117 1.756468 -6.500000
    endloop
  endfacet
  facet normal -0.827690 -0.561186 -0.000000
    outer loop
      vertex 6.446072 1.644442 -4.500000
      vertex 6.370117 1.756468 -6.500000
      vertex 6.446072 1.644442 -6.500000
    endloop
  endfacet
  facet normal -0.883512 -0.468409 0.000000
    outer loop
      vertex 6.509470 1.524861 -4.500000
      vertex 6.446072 1.644442 -4.500000
      vertex 6.446072 1.644442 -6.500000
    endloop
  endfacet
  facet normal -0.883512 -0.468409 -0.000000
    outer loop
      vertex 6.509470 1.524861 -4.500000
      vertex 6.446072 1.644442 -6.500000
      vertex 6.509470 1.524861 -6.500000
    endloop
  endfacet
  facet normal -0.928977 -0.370137 0.000000
    outer loop
      vertex 6.559566 1.399127 -4.500000
      vertex 6.509470 1.524861 -4.500000
      vertex 6.509470 1.524861 -6.500000
    endloop
  endfacet
  facet normal -0.928977 -0.370137 -0.000000
    outer loop
      vertex 6.559566 1.399127 -4.500000
      vertex 6.509470 1.524861 -6.500000
      vertex 6.559566 1.399127 -6.500000
    endloop
  endfacet
  facet normal -0.963550 -0.267527 0.000000
    outer loop
      vertex 6.595776 1.268713 -4.500000
      vertex 6.559566 1.399127 -4.500000
      vertex 6.559566 1.399127 -6.500000
    endloop
  endfacet
  facet normal -0.963550 -0.267527 -0.000000
    outer loop
      vertex 6.595776 1.268713 -4.500000
      vertex 6.559566 1.399127 -6.500000
      vertex 6.595776 1.268713 -6.500000
    endloop
  endfacet
  facet normal -0.986826 -0.161783 0.000000
    outer loop
      vertex 6.617672 1.135149 -4.500000
      vertex 6.595776 1.268713 -4.500000
      vertex 6.595776 1.268713 -6.500000
    endloop
  endfacet
  facet normal -0.986826 -0.161783 -0.000000
    outer loop
      vertex 6.617672 1.135149 -4.500000
      vertex 6.595776 1.268713 -6.500000
      vertex 6.617672 1.135149 -6.500000
    endloop
  endfacet
  facet normal -0.998533 -0.054139 0.000000
    outer loop
      vertex 6.625000 1.000000 -4.500000
      vertex 6.617672 1.135149 -4.500000
      vertex 6.617672 1.135149 -6.500000
    endloop
  endfacet
  facet normal -0.998533 -0.054139 -0.000000
    outer loop
      vertex 6.625000 1.000000 -4.500000
      vertex 6.617672 1.135149 -6.500000
      vertex 6.625000 1.000000 -6.500000
    endloop
  endfacet
  facet normal -0.998533 0.054139 0.000000
    outer loop
      vertex 6.617672 0.864851 -4.500000
      vertex 6.625000 1.000000 -4.500000
      vertex 6.625000 1.000000 -6.500000
    endloop
  endfacet
  facet normal -0.998533 0.054139 0.000000
    outer loop
      vertex 6.617672 0.864851 -4.500000
      vertex 6.625000 1.000000 -6.500000
      vertex 6.617672 0.864851 -6.500000
    endloop
  endfacet
  facet normal -0.986826 0.161783 0.000000
    outer loop
      vertex 6.595776 0.731287 -4.500000
      vertex 6.617672 0.864851 -4.500000
      vertex 6.617672 0.864851 -6.500000
    endloop
  endfacet
  facet normal -0.986826 0.161783 0.000000
    outer loop
      vertex 6.595776 0.731287 -4.500000
      vertex 6.617672 0.864851 -6.500000
      vertex 6.595776 0.731287 -6.500000
    endloop
  endfacet
  facet normal -0.963550 0.267528 0.000000
    outer loop
      vertex 6.559566 0.600873 -4.500000
      vertex 6.595776 0.731287 -4.500000
      vertex 6.595776 0.731287 -6.500000
    endloop
  endfacet
  facet normal -0.963550 0.267528 0.000000
    outer loop
      vertex 6.559566 0.600873 -4.500000
      vertex 6.595776 0.731287 -6.500000
      vertex 6.559566 0.600873 -6.500000
    endloop
  endfacet
  facet normal -0.928977 0.370137 0.000000
    outer loop
      vertex 6.509470 0.475139 -4.500000
      vertex 6.559566 0.600873 -4.500000
      vertex 6.559566 0.600873 -6.500000
    endloop
  endfacet
  facet normal -0.928977 0.370137 0.000000
    outer loop
      vertex 6.509470 0.475139 -4.500000
      vertex 6.559566 0.600873 -6.500000
      vertex 6.509470 0.475139 -6.500000
    endloop
  endfacet
  facet normal -0.883512 0.468409 0.000000
    outer loop
      vertex 6.446072 0.355558 -4.500000
      vertex 6.509470 0.475139 -4.500000
      vertex 6.509470 0.475139 -6.500000
    endloop
  endfacet
  facet normal -0.883512 0.468409 0.000000
    outer loop
      vertex 6.446072 0.355558 -4.500000
      vertex 6.509470 0.475139 -6.500000
      vertex 6.446072 0.355558 -6.500000
    endloop
  endfacet
  facet normal -0.827690 0.561186 0.000000
    outer loop
      vertex 6.370117 0.243532 -4.500000
      vertex 6.446072 0.355558 -4.500000
      vertex 6.446072 0.355558 -6.500000
    endloop
  endfacet
  facet normal -0.827690 0.561186 0.000000
    outer loop
      vertex 6.370117 0.243532 -4.500000
      vertex 6.446072 0.355558 -6.500000
      vertex 6.370117 0.243532 -6.500000
    endloop
  endfacet
  facet normal -0.762161 0.647387 0.000000
    outer loop
      vertex 6.282495 0.140376 -4.500000
      vertex 6.370117 0.243532 -4.500000
      vertex 6.370117 0.243532 -6.500000
    endloop
  endfacet
  facet normal -0.762161 0.647387 0.000000
    outer loop
      vertex 6.282495 0.140376 -4.500000
      vertex 6.370117 0.243532 -6.500000
      vertex 6.282495 0.140376 -6.500000
    endloop
  endfacet
  facet normal -0.687698 0.725997 0.000000
    outer loop
      vertex 6.184233 0.047297 -4.500000
      vertex 6.282495 0.140376 -4.500000
      vertex 6.282495 0.140376 -6.500000
    endloop
  endfacet
  facet normal -0.687698 0.725997 0.000000
    outer loop
      vertex 6.184233 0.047297 -4.500000
      vertex 6.282495 0.140376 -6.500000
      vertex 6.184233 0.047297 -6.500000
    endloop
  endfacet
  facet normal -0.605176 0.796092 0.000000
    outer loop
      vertex 6.076484 -0.034611 -4.500000
      vertex 6.184233 0.047297 -4.500000
      vertex 6.184233 0.047297 -6.500000
    endloop
  endfacet
  facet normal -0.605176 0.796092 0.000000
    outer loop
      vertex 6.076484 -0.034611 -4.500000
      vertex 6.184233 0.047297 -6.500000
      vertex 6.076484 -0.034611 -6.500000
    endloop
  endfacet
  facet normal -0.515553 0.856858 0.000000
    outer loop
      vertex 5.960511 -0.104390 -4.500000
      vertex 6.076484 -0.034611 -4.500000
      vertex 6.076484 -0.034611 -6.500000
    endloop
  endfacet
  facet normal -0.515553 0.856858 0.000000
    outer loop
      vertex 5.960511 -0.104390 -4.500000
      vertex 6.076484 -0.034611 -6.500000
      vertex 5.960511 -0.104390 -6.500000
    endloop
  endfacet
  facet normal -0.419889 0.907576 0.000000
    outer loop
      vertex 5.837673 -0.161221 -4.500000
      vertex 5.960511 -0.104390 -4.500000
      vertex 5.960511 -0.104390 -6.500000
    endloop
  endfacet
  facet normal -0.419889 0.907576 0.000000
    outer loop
      vertex 5.837673 -0.161221 -4.500000
      vertex 5.960511 -0.104390 -6.500000
      vertex 5.837673 -0.161221 -6.500000
    endloop
  endfacet
  facet normal -0.319302 0.947653 0.000000
    outer loop
      vertex 5.709411 -0.204437 -4.500000
      vertex 5.837673 -0.161221 -4.500000
      vertex 5.837673 -0.161221 -6.500000
    endloop
  endfacet
  facet normal -0.319302 0.947653 0.000000
    outer loop
      vertex 5.709411 -0.204437 -4.500000
      vertex 5.837673 -0.161221 -6.500000
      vertex 5.709411 -0.204437 -6.500000
    endloop
  endfacet
  facet normal -0.214970 0.976621 0.000000
    outer loop
      vertex 5.577228 -0.233533 -4.500000
      vertex 5.709411 -0.204437 -4.500000
      vertex 5.709411 -0.204437 -6.500000
    endloop
  endfacet
  facet normal -0.214970 0.976621 0.000000
    outer loop
      vertex 5.577228 -0.233533 -4.500000
      vertex 5.709411 -0.204437 -6.500000
      vertex 5.577228 -0.233533 -6.500000
    endloop
  endfacet
  facet normal -0.108119 0.994138 0.000000
    outer loop
      vertex 5.442674 -0.248167 -4.500000
      vertex 5.577228 -0.233533 -4.500000
      vertex 5.577228 -0.233533 -6.500000
    endloop
  endfacet
  facet normal -0.108119 0.994138 0.000000
    outer loop
      vertex 5.442674 -0.248167 -4.500000
      vertex 5.577228 -0.233533 -6.500000
      vertex 5.442674 -0.248167 -6.500000
    endloop
  endfacet
  facet normal -0.000000 1.000000 0.000000
    outer loop
      vertex 5.307327 -0.248167 -4.500000
      vertex 5.442674 -0.248167 -4.500000
      vertex 5.442674 -0.248167 -6.500000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 5.307327 -0.248167 -4.500000
      vertex 5.442674 -0.248167 -6.500000
      vertex 5.307327 -0.248167 -6.500000
    endloop
  endfacet
  facet normal 0.108118 0.994138 0.000000
    outer loop
      vertex 5.172772 -0.233533 -4.500000
      vertex 5.307327 -0.248167 -4.500000
      vertex 5.307327 -0.248167 -6.500000
    endloop
  endfacet
  facet normal 0.108118 0.994138 0.000000
    outer loop
      vertex 5.172772 -0.233533 -4.500000
      vertex 5.307327 -0.248167 -6.500000
      vertex 5.172772 -0.233533 -6.500000
    endloop
  endfacet
  facet normal 0.214971 0.976620 0.000000
    outer loop
      vertex 5.040590 -0.204437 -4.500000
      vertex 5.172772 -0.233533 -4.500000
      vertex 5.172772 -0.233533 -6.500000
    endloop
  endfacet
  facet normal 0.214971 0.976620 0.000000
    outer loop
      vertex 5.040590 -0.204437 -4.500000
      vertex 5.172772 -0.233533 -6.500000
      vertex 5.040590 -0.204437 -6.500000
    endloop
  endfacet
  facet normal 0.319301 0.947653 0.000000
    outer loop
      vertex 4.912327 -0.161221 -4.500000
      vertex 5.040590 -0.204437 -4.500000
      vertex 5.040590 -0.204437 -6.500000
    endloop
  endfacet
  facet normal 0.319301 0.947653 0.000000
    outer loop
      vertex 4.912327 -0.161221 -4.500000
      vertex 5.040590 -0.204437 -6.500000
      vertex 4.912327 -0.161221 -6.500000
    endloop
  endfacet
  facet normal 0.419889 0.907576 0.000000
    outer loop
      vertex 4.789489 -0.104390 -4.500000
      vertex 4.912327 -0.161221 -4.500000
      vertex 4.912327 -0.161221 -6.500000
    endloop
  endfacet
  facet normal 0.419889 0.907576 0.000000
    outer loop
      vertex 4.789489 -0.104390 -4.500000
      vertex 4.912327 -0.161221 -6.500000
      vertex 4.789489 -0.104390 -6.500000
    endloop
  endfacet
  facet normal 0.515555 0.856857 0.000000
    outer loop
      vertex 4.673516 -0.034611 -4.500000
      vertex 4.789489 -0.104390 -4.500000
      vertex 4.789489 -0.104390 -6.500000
    endloop
  endfacet
  facet normal 0.515555 0.856857 0.000000
    outer loop
      vertex 4.673516 -0.034611 -4.500000
      vertex 4.789489 -0.104390 -6.500000
      vertex 4.673516 -0.034611 -6.500000
    endloop
  endfacet
  facet normal 0.605173 0.796094 0.000000
    outer loop
      vertex 4.565767 0.047297 -4.500000
      vertex 4.673516 -0.034611 -4.500000
      vertex 4.673516 -0.034611 -6.500000
    endloop
  endfacet
  facet normal 0.605173 0.796094 0.000000
    outer loop
      vertex 4.565767 0.047297 -4.500000
      vertex 4.673516 -0.034611 -6.500000
      vertex 4.565767 0.047297 -6.500000
    endloop
  endfacet
  facet normal 0.687700 0.725995 0.000000
    outer loop
      vertex 4.467505 0.140376 -4.500000
      vertex 4.565767 0.047297 -4.500000
      vertex 4.565767 0.047297 -6.500000
    endloop
  endfacet
  facet normal 0.687700 0.725995 0.000000
    outer loop
      vertex 4.467505 0.140376 -4.500000
      vertex 4.565767 0.047297 -6.500000
      vertex 4.467505 0.140376 -6.500000
    endloop
  endfacet
  facet normal 0.762163 0.647385 0.000000
    outer loop
      vertex 4.379884 0.243532 -4.500000
      vertex 4.467505 0.140376 -4.500000
      vertex 4.467505 0.140376 -6.500000
    endloop
  endfacet
  facet normal 0.762163 0.647385 0.000000
    outer loop
      vertex 4.379884 0.243532 -4.500000
      vertex 4.467505 0.140376 -6.500000
      vertex 4.379884 0.243532 -6.500000
    endloop
  endfacet
  facet normal 0.827688 0.561188 0.000000
    outer loop
      vertex 4.303928 0.355558 -4.500000
      vertex 4.379884 0.243532 -4.500000
      vertex 4.379884 0.243532 -6.500000
    endloop
  endfacet
  facet normal 0.827688 0.561188 0.000000
    outer loop
      vertex 4.303928 0.355558 -4.500000
      vertex 4.379884 0.243532 -6.500000
      vertex 4.303928 0.355558 -6.500000
    endloop
  endfacet
  facet normal 0.883512 0.468409 0.000000
    outer loop
      vertex 4.240530 0.475139 -4.500000
      vertex 4.303928 0.355558 -4.500000
      vertex 4.303928 0.355558 -6.500000
    endloop
  endfacet
  facet normal 0.883512 0.468409 0.000000
    outer loop
      vertex 4.240530 0.475139 -4.500000
      vertex 4.303928 0.355558 -6.500000
      vertex 4.240530 0.475139 -6.500000
    endloop
  endfacet
  facet normal 0.928977 0.370137 0.000000
    outer loop
      vertex 4.190434 0.600873 -4.500000
      vertex 4.240530 0.475139 -4.500000
      vertex 4.240530 0.475139 -6.500000
    endloop
  endfacet
  facet normal 0.928977 0.370137 0.000000
    outer loop
      vertex 4.190434 0.600873 -4.500000
      vertex 4.240530 0.475139 -6.500000
      vertex 4.190434 0.600873 -6.500000
    endloop
  endfacet
  facet normal 0.963550 0.267528 0.000000
    outer loop
      vertex 4.154224 0.731287 -4.500000
      vertex 4.190434 0.600873 -4.500000
      vertex 4.190434 0.600873 -6.500000
    endloop
  endfacet
  facet normal 0.963550 0.267528 0.000000
    outer loop
      vertex 4.154224 0.731287 -4.500000
      vertex 4.190434 0.600873 -6.500000
      vertex 4.154224 0.731287 -6.500000
    endloop
  endfacet
  facet normal 0.986826 0.161783 0.000000
    outer loop
      vertex 4.132328 0.864851 -4.500000
      vertex 4.154224 0.731287 -4.500000
      vertex 4.154224 0.731287 -6.500000
    endloop
  endfacet
  facet normal 0.986826 0.161783 0.000000
    outer loop
      vertex 4.132328 0.864851 -4.500000
      vertex 4.154224 0.731287 -6.500000
      vertex 4.132328 0.864851 -6.500000
    endloop
  endfacet
  facet normal 0.998533 0.054139 0.000000
    outer loop
      vertex 4.125000 1.000000 -4.500000
      vertex 4.132328 0.864851 -4.500000
      vertex 4.132328 0.864851 -6.500000
    endloop
  endfacet
  facet normal 0.998533 0.054139 0.000000
    outer loop
      vertex 4.125000 1.000000 -4.500000
      vertex 4.132328 0.864851 -6.500000
      vertex 4.125000 1.000000 -6.500000
    endloop
  endfacet
  facet normal 0.998534 -0.054128 0.000000
    outer loop
      vertex 24.382326 1.135149 -4.500000
      vertex 24.375000 1.000000 -4.500000
      vertex 24.375000 1.000000 -6.500000
    endloop
  endfacet
  facet normal 0.998534 -0.054128 0.000000
    outer loop
      vertex 24.382326 1.135149 -4.500000
      vertex 24.375000 1.000000 -6.500000
      vertex 24.382326 1.135149 -6.500000
    endloop
  endfacet
  facet normal 0.986825 -0.161793 0.000000
    outer loop
      vertex 24.404224 1.268713 -4.500000
      vertex 24.382326 1.135149 -4.500000
      vertex 24.382326 1.135149 -6.500000
    endloop
  endfacet
  facet normal 0.986825 -0.161793 0.000000
    outer loop
      vertex 24.404224 1.268713 -4.500000
      vertex 24.382326 1.135149 -6.500000
      vertex 24.404224 1.268713 -6.500000
    endloop
  endfacet
  facet normal 0.963550 -0.267527 0.000000
    outer loop
      vertex 24.440434 1.399127 -4.500000
      vertex 24.404224 1.268713 -4.500000
      vertex 24.404224 1.268713 -6.500000
    endloop
  endfacet
  facet normal 0.963550 -0.267527 0.000000
    outer loop
      vertex 24.440434 1.399127 -4.500000
      vertex 24.404224 1.268713 -6.500000
      vertex 24.440434 1.399127 -6.500000
    endloop
  endfacet
  facet normal 0.928973 -0.370146 0.000000
    outer loop
      vertex 24.490532 1.524861 -4.500000
      vertex 24.440434 1.399127 -4.500000
      vertex 24.440434 1.399127 -6.500000
    endloop
  endfacet
  facet normal 0.928973 -0.370146 0.000000
    outer loop
      vertex 24.490532 1.524861 -4.500000
      vertex 24.440434 1.399127 -6.500000
      vertex 24.490532 1.524861 -6.500000
    endloop
  endfacet
  facet normal 0.883516 -0.468401 0.000000
    outer loop
      vertex 24.553928 1.644442 -4.500000
      vertex 24.490532 1.524861 -4.500000
      vertex 24.490532 1.524861 -6.500000
    endloop
  endfacet
  facet normal 0.883516 -0.468401 0.000000
    outer loop
      vertex 24.553928 1.644442 -4.500000
      vertex 24.490532 1.524861 -6.500000
      vertex 24.553928 1.644442 -6.500000
    endloop
  endfacet
  facet normal 0.827691 -0.561184 0.000000
    outer loop
      vertex 24.629883 1.756468 -4.500000
      vertex 24.553928 1.644442 -4.500000
      vertex 24.553928 1.644442 -6.500000
    endloop
  endfacet
  facet normal 0.827691 -0.561184 0.000000
    outer loop
      vertex 24.629883 1.756468 -4.500000
      vertex 24.553928 1.644442 -6.500000
      vertex 24.629883 1.756468 -6.500000
    endloop
  endfacet
  facet normal 0.762156 -0.647393 0.000000
    outer loop
      vertex 24.717506 1.859624 -4.500000
      vertex 24.629883 1.756468 -4.500000
      vertex 24.629883 1.756468 -6.500000
    endloop
  endfacet
  facet normal 0.762156 -0.647393 0.000000
    outer loop
      vertex 24.717506 1.859624 -4.500000
      vertex 24.629883 1.756468 -6.500000
      vertex 24.717506 1.859624 -6.500000
    endloop
  endfacet
  facet normal 0.687702 -0.725993 0.000000
    outer loop
      vertex 24.815767 1.952703 -4.500000
      vertex 24.717506 1.859624 -4.500000
      vertex 24.717506 1.859624 -6.500000
    endloop
  endfacet
  facet normal 0.687702 -0.725993 0.000000
    outer loop
      vertex 24.815767 1.952703 -4.500000
      vertex 24.717506 1.859624 -6.500000
      vertex 24.815767 1.952703 -6.500000
    endloop
  endfacet
  facet normal 0.605171 -0.796095 0.000000
    outer loop
      vertex 24.923517 2.034611 -4.500000
      vertex 24.815767 1.952703 -4.500000
      vertex 24.815767 1.952703 -6.500000
    endloop
  endfacet
  facet normal 0.605171 -0.796095 0.000000
    outer loop
      vertex 24.923517 2.034611 -4.500000
      vertex 24.815767 1.952703 -6.500000
      vertex 24.923517 2.034611 -6.500000
    endloop
  endfacet
  facet normal 0.515556 -0.856856 0.000000
    outer loop
      vertex 25.039490 2.104390 -4.500000
      vertex 24.923517 2.034611 -4.500000
      vertex 24.923517 2.034611 -6.500000
    endloop
  endfacet
  facet normal 0.515556 -0.856856 0.000000
    outer loop
      vertex 25.039490 2.104390 -4.500000
      vertex 24.923517 2.034611 -6.500000
      vertex 25.039490 2.104390 -6.500000
    endloop
  endfacet
  facet normal 0.419886 -0.907577 0.000000
    outer loop
      vertex 25.162329 2.161221 -4.500000
      vertex 25.039490 2.104390 -4.500000
      vertex 25.039490 2.104390 -6.500000
    endloop
  endfacet
  facet normal 0.419886 -0.907577 0.000000
    outer loop
      vertex 25.162329 2.161221 -4.500000
      vertex 25.039490 2.104390 -6.500000
      vertex 25.162329 2.161221 -6.500000
    endloop
  endfacet
  facet normal 0.319304 -0.947652 0.000000
    outer loop
      vertex 25.290590 2.204437 -4.500000
      vertex 25.162329 2.161221 -4.500000
      vertex 25.162329 2.161221 -6.500000
    endloop
  endfacet
  facet normal 0.319304 -0.947652 0.000000
    outer loop
      vertex 25.290590 2.204437 -4.500000
      vertex 25.162329 2.161221 -6.500000
      vertex 25.290590 2.204437 -6.500000
    endloop
  endfacet
  facet normal 0.214973 -0.976620 0.000000
    outer loop
      vertex 25.422771 2.233533 -4.500000
      vertex 25.290590 2.204437 -4.500000
      vertex 25.290590 2.204437 -6.500000
    endloop
  endfacet
  facet normal 0.214973 -0.976620 0.000000
    outer loop
      vertex 25.422771 2.233533 -4.500000
      vertex 25.290590 2.204437 -6.500000
      vertex 25.422771 2.233533 -6.500000
    endloop
  endfacet
  facet normal 0.108119 -0.994138 0.000000
    outer loop
      vertex 25.557325 2.248167 -4.500000
      vertex 25.422771 2.233533 -4.500000
      vertex 25.422771 2.233533 -6.500000
    endloop
  endfacet
  facet normal 0.108119 -0.994138 0.000000
    outer loop
      vertex 25.557325 2.248167 -4.500000
      vertex 25.422771 2.233533 -6.500000
      vertex 25.557325 2.248167 -6.500000
    endloop
  endfacet
  facet normal -0.000000 -1.000000 0.000000
    outer loop
      vertex 25.692673 2.248167 -4.500000
      vertex 25.557325 2.248167 -4.500000
      vertex 25.557325 2.248167 -6.500000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 -0.000000
    outer loop
      vertex 25.692673 2.248167 -4.500000
      vertex 25.557325 2.248167 -6.500000
      vertex 25.692673 2.248167 -6.500000
    endloop
  endfacet
  facet normal -0.108119 -0.994138 0.000000
    outer loop
      vertex 25.827227 2.233533 -4.500000
      vertex 25.692673 2.248167 -4.500000
      vertex 25.692673 2.248167 -6.500000
    endloop
  endfacet
  facet normal -0.108119 -0.994138 -0.000000
    outer loop
      vertex 25.827227 2.233533 -4.500000
      vertex 25.692673 2.248167 -6.500000
      vertex 25.827227 2.233533 -6.500000
    endloop
  endfacet
  facet normal -0.214970 -0.976621 0.000000
    outer loop
      vertex 25.959410 2.204437 -4.500000
      vertex 25.827227 2.233533 -4.500000
      vertex 25.827227 2.233533 -6.500000
    endloop
  endfacet
  facet normal -0.214970 -0.976621 -0.000000
    outer loop
      vertex 25.959410 2.204437 -4.500000
      vertex 25.827227 2.233533 -6.500000
      vertex 25.959410 2.204437 -6.500000
    endloop
  endfacet
  facet normal -0.319300 -0.947654 0.000000
    outer loop
      vertex 26.087673 2.161221 -4.500000
      vertex 25.959410 2.204437 -4.500000
      vertex 25.959410 2.204437 -6.500000
    endloop
  endfacet
  facet normal -0.319300 -0.947654 -0.000000
    outer loop
      vertex 26.087673 2.161221 -4.500000
      vertex 25.959410 2.204437 -6.500000
      vertex 26.087673 2.161221 -6.500000
    endloop
  endfacet
  facet normal -0.419892 -0.907574 0.000000
    outer loop
      vertex 26.210510 2.104390 -4.500000
      vertex 26.087673 2.161221 -4.500000
      vertex 26.087673 2.161221 -6.500000
    endloop
  endfacet
  facet normal -0.419892 -0.907574 -0.000000
    outer loop
      vertex 26.210510 2.104390 -4.500000
      vertex 26.087673 2.161221 -6.500000
      vertex 26.210510 2.104390 -6.500000
    endloop
  endfacet
  facet normal -0.515556 -0.856856 0.000000
    outer loop
      vertex 26.326483 2.034611 -4.500000
      vertex 26.210510 2.104390 -4.500000
      vertex 26.210510 2.104390 -6.500000
    endloop
  endfacet
  facet normal -0.515556 -0.856856 -0.000000
    outer loop
      vertex 26.326483 2.034611 -4.500000
      vertex 26.210510 2.104390 -6.500000
      vertex 26.326483 2.034611 -6.500000
    endloop
  endfacet
  facet normal -0.605171 -0.796095 0.000000
    outer loop
      vertex 26.434233 1.952703 -4.500000
      vertex 26.326483 2.034611 -4.500000
      vertex 26.326483 2.034611 -6.500000
    endloop
  endfacet
  facet normal -0.605171 -0.796095 -0.000000
    outer loop
      vertex 26.434233 1.952703 -4.500000
      vertex 26.326483 2.034611 -6.500000
      vertex 26.434233 1.952703 -6.500000
    endloop
  endfacet
  facet normal -0.687702 -0.725993 0.000000
    outer loop
      vertex 26.532494 1.859624 -4.500000
      vertex 26.434233 1.952703 -4.500000
      vertex 26.434233 1.952703 -6.500000
    endloop
  endfacet
  facet normal -0.687702 -0.725993 -0.000000
    outer loop
      vertex 26.532494 1.859624 -4.500000
      vertex 26.434233 1.952703 -6.500000
      vertex 26.532494 1.859624 -6.500000
    endloop
  endfacet
  facet normal -0.762163 -0.647385 0.000000
    outer loop
      vertex 26.620115 1.756468 -4.500000
      vertex 26.532494 1.859624 -4.500000
      vertex 26.532494 1.859624 -6.500000
    endloop
  endfacet
  facet normal -0.762163 -0.647385 -0.000000
    outer loop
      vertex 26.620115 1.756468 -4.500000
      vertex 26.532494 1.859624 -6.500000
      vertex 26.620115 1.756468 -6.500000
    endloop
  endfacet
  facet normal -0.827685 -0.561193 0.000000
    outer loop
      vertex 26.696072 1.644442 -4.500000
      vertex 26.620115 1.756468 -4.500000
      vertex 26.620115 1.756468 -6.500000
    endloop
  endfacet
  facet normal -0.827685 -0.561193 -0.000000
    outer loop
      vertex 26.696072 1.644442 -4.500000
      vertex 26.620115 1.756468 -6.500000
      vertex 26.696072 1.644442 -6.500000
    endloop
  endfacet
  facet normal -0.883510 -0.468412 0.000000
    outer loop
      vertex 26.759470 1.524861 -4.500000
      vertex 26.696072 1.644442 -4.500000
      vertex 26.696072 1.644442 -6.500000
    endloop
  endfacet
  facet normal -0.883510 -0.468412 -0.000000
    outer loop
      vertex 26.759470 1.524861 -4.500000
      vertex 26.696072 1.644442 -6.500000
      vertex 26.759470 1.524861 -6.500000
    endloop
  endfacet
  facet normal -0.928978 -0.370134 0.000000
    outer loop
      vertex 26.809566 1.399127 -4.500000
      vertex 26.759470 1.524861 -4.500000
      vertex 26.759470 1.524861 -6.500000
    endloop
  endfacet
  facet normal -0.928978 -0.370134 -0.000000
    outer loop
      vertex 26.809566 1.399127 -4.500000
      vertex 26.759470 1.524861 -6.500000
      vertex 26.809566 1.399127 -6.500000
    endloop
  endfacet
  facet normal -0.963550 -0.267527 0.000000
    outer loop
      vertex 26.845776 1.268713 -4.500000
      vertex 26.809566 1.399127 -4.500000
      vertex 26.809566 1.399127 -6.500000
    endloop
  endfacet
  facet normal -0.963550 -0.267527 -0.000000
    outer loop
      vertex 26.845776 1.268713 -4.500000
      vertex 26.809566 1.399127 -6.500000
      vertex 26.845776 1.268713 -6.500000
    endloop
  endfacet
  facet normal -0.986827 -0.161779 0.000000
    outer loop
      vertex 26.867672 1.135149 -4.500000
      vertex 26.845776 1.268713 -4.500000
      vertex 26.845776 1.268713 -6.500000
    endloop
  endfacet
  facet normal -0.986827 -0.161779 -0.000000
    outer loop
      vertex 26.867672 1.135149 -4.500000
      vertex 26.845776 1.268713 -6.500000
      vertex 26.867672 1.135149 -6.500000
    endloop
  endfacet
  facet normal -0.998533 -0.054142 0.000000
    outer loop
      vertex 26.875000 1.000000 -4.500000
      vertex 26.867672 1.135149 -4.500000
      vertex 26.867672 1.135149 -6.500000
    endloop
  endfacet
  facet normal -0.998533 -0.054142 -0.000000
    outer loop
      vertex 26.875000 1.000000 -4.500000
      vertex 26.867672 1.135149 -6.500000
      vertex 26.875000 1.000000 -6.500000
    endloop
  endfacet
  facet normal -0.998533 0.054142 0.000000
    outer loop
      vertex 26.867672 0.864851 -4.500000
      vertex 26.875000 1.000000 -4.500000
      vertex 26.875000 1.000000 -6.500000
    endloop
  endfacet
  facet normal -0.998533 0.054142 0.000000
    outer loop
      vertex 26.867672 0.864851 -4.500000
      vertex 26.875000 1.000000 -6.500000
      vertex 26.867672 0.864851 -6.500000
    endloop
  endfacet
  facet normal -0.986827 0.161779 0.000000
    outer loop
      vertex 26.845776 0.731287 -4.500000
      vertex 26.867672 0.864851 -4.500000
      vertex 26.867672 0.864851 -6.500000
    endloop
  endfacet
  facet normal -0.986827 0.161779 0.000000
    outer loop
      vertex 26.845776 0.731287 -4.500000
      vertex 26.867672 0.864851 -6.500000
      vertex 26.845776 0.731287 -6.500000
    endloop
  endfacet
  facet normal -0.963550 0.267528 0.000000
    outer loop
      vertex 26.809566 0.600873 -4.500000
      vertex 26.845776 0.731287 -4.500000
      vertex 26.845776 0.731287 -6.500000
    endloop
  endfacet
  facet normal -0.963550 0.267528 0.000000
    outer loop
      vertex 26.809566 0.600873 -4.500000
      vertex 26.845776 0.731287 -6.500000
      vertex 26.809566 0.600873 -6.500000
    endloop
  endfacet
  facet normal -0.928978 0.370134 0.000000
    outer loop
      vertex 26.759470 0.475139 -4.500000
      vertex 26.809566 0.600873 -4.500000
      vertex 26.809566 0.600873 -6.500000
    endloop
  endfacet
  facet normal -0.928978 0.370134 0.000000
    outer loop
      vertex 26.759470 0.475139 -4.500000
      vertex 26.809566 0.600873 -6.500000
      vertex 26.759470 0.475139 -6.500000
    endloop
  endfacet
  facet normal -0.883510 0.468412 0.000000
    outer loop
      vertex 26.696072 0.355558 -4.500000
      vertex 26.759470 0.475139 -4.500000
      vertex 26.759470 0.475139 -6.500000
    endloop
  endfacet
  facet normal -0.883510 0.468412 0.000000
    outer loop
      vertex 26.696072 0.355558 -4.500000
      vertex 26.759470 0.475139 -6.500000
      vertex 26.696072 0.355558 -6.500000
    endloop
  endfacet
  facet normal -0.827685 0.561193 0.000000
    outer loop
      vertex 26.620115 0.243532 -4.500000
      vertex 26.696072 0.355558 -4.500000
      vertex 26.696072 0.355558 -6.500000
    endloop
  endfacet
  facet normal -0.827685 0.561193 0.000000
    outer loop
      vertex 26.620115 0.243532 -4.500000
      vertex 26.696072 0.355558 -6.500000
      vertex 26.620115 0.243532 -6.500000
    endloop
  endfacet
  facet normal -0.762163 0.647385 0.000000
    outer loop
      vertex 26.532494 0.140376 -4.500000
      vertex 26.620115 0.243532 -4.500000
      vertex 26.620115 0.243532 -6.500000
    endloop
  endfacet
  facet normal -0.762163 0.647385 0.000000
    outer loop
      vertex 26.532494 0.140376 -4.500000
      vertex 26.620115 0.243532 -6.500000
      vertex 26.532494 0.140376 -6.500000
    endloop
  endfacet
  facet normal -0.687702 0.725993 0.000000
    outer loop
      vertex 26.434233 0.047297 -4.500000
      vertex 26.532494 0.140376 -4.500000
      vertex 26.532494 0.140376 -6.500000
    endloop
  endfacet
  facet normal -0.687702 0.725993 0.000000
    outer loop
      vertex 26.434233 0.047297 -4.500000
      vertex 26.532494 0.140376 -6.500000
      vertex 26.434233 0.047297 -6.500000
    endloop
  endfacet
  facet normal -0.605171 0.796095 0.000000
    outer loop
      vertex 26.326483 -0.034611 -4.500000
      vertex 26.434233 0.047297 -4.500000
      vertex 26.434233 0.047297 -6.500000
    endloop
  endfacet
  facet normal -0.605171 0.796095 0.000000
    outer loop
      vertex 26.326483 -0.034611 -4.500000
      vertex 26.434233 0.047297 -6.500000
      vertex 26.326483 -0.034611 -6.500000
    endloop
  endfacet
  facet normal -0.515556 0.856856 0.000000
    outer loop
      vertex 26.210510 -0.104390 -4.500000
      vertex 26.326483 -0.034611 -4.500000
      vertex 26.326483 -0.034611 -6.500000
    endloop
  endfacet
  facet normal -0.515556 0.856856 0.000000
    outer loop
      vertex 26.210510 -0.104390 -4.500000
      vertex 26.326483 -0.034611 -6.500000
      vertex 26.210510 -0.104390 -6.500000
    endloop
  endfacet
  facet normal -0.419891 0.907574 0.000000
    outer loop
      vertex 26.087673 -0.161221 -4.500000
      vertex 26.210510 -0.104390 -4.500000
      vertex 26.210510 -0.104390 -6.500000
    endloop
  endfacet
  facet normal -0.419891 0.907574 0.000000
    outer loop
      vertex 26.087673 -0.161221 -4.500000
      vertex 26.210510 -0.104390 -6.500000
      vertex 26.087673 -0.161221 -6.500000
    endloop
  endfacet
  facet normal -0.319299 0.947654 0.000000
    outer loop
      vertex 25.959410 -0.204437 -4.500000
      vertex 26.087673 -0.161221 -4.500000
      vertex 26.087673 -0.161221 -6.500000
    endloop
  endfacet
  facet normal -0.319299 0.947654 0.000000
    outer loop
      vertex 25.959410 -0.204437 -4.500000
      vertex 26.087673 -0.161221 -6.500000
      vertex 25.959410 -0.204437 -6.500000
    endloop
  endfacet
  facet normal -0.214970 0.976621 0.000000
    outer loop
      vertex 25.827227 -0.233533 -4.500000
      vertex 25.959410 -0.204437 -4.500000
      vertex 25.959410 -0.204437 -6.500000
    endloop
  endfacet
  facet normal -0.214970 0.976621 0.000000
    outer loop
      vertex 25.827227 -0.233533 -4.500000
      vertex 25.959410 -0.204437 -6.500000
      vertex 25.827227 -0.233533 -6.500000
    endloop
  endfacet
  facet normal -0.108119 0.994138 0.000000
    outer loop
      vertex 25.692673 -0.248167 -4.500000
      vertex 25.827227 -0.233533 -4.500000
      vertex 25.827227 -0.233533 -6.500000
    endloop
  endfacet
  facet normal -0.108119 0.994138 0.000000
    outer loop
      vertex 25.692673 -0.248167 -4.500000
      vertex 25.827227 -0.233533 -6.500000
      vertex 25.692673 -0.248167 -6.500000
    endloop
  endfacet
  facet normal -0.000000 1.000000 0.000000
    outer loop
      vertex 25.557325 -0.248167 -4.500000
      vertex 25.692673 -0.248167 -4.500000
      vertex 25.692673 -0.248167 -6.500000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 25.557325 -0.248167 -4.500000
      vertex 25.692673 -0.248167 -6.500000
      vertex 25.557325 -0.248167 -6.500000
    endloop
  endfacet
  facet normal 0.108119 0.994138 0.000000
    outer loop
      vertex 25.422771 -0.233533 -4.500000
      vertex 25.557325 -0.248167 -4.500000
      vertex 25.557325 -0.248167 -6.500000
    endloop
  endfacet
  facet normal 0.108119 0.994138 0.000000
    outer loop
      vertex 25.422771 -0.233533 -4.500000
      vertex 25.557325 -0.248167 -6.500000
      vertex 25.422771 -0.233533 -6.500000
    endloop
  endfacet
  facet normal 0.214973 0.976620 0.000000
    outer loop
      vertex 25.290590 -0.204437 -4.500000
      vertex 25.422771 -0.233533 -4.500000
      vertex 25.422771 -0.233533 -6.500000
    endloop
  endfacet
  facet normal 0.214973 0.976620 0.000000
    outer loop
      vertex 25.290590 -0.204437 -4.500000
      vertex 25.422771 -0.233533 -6.500000
      vertex 25.290590 -0.204437 -6.500000
    endloop
  endfacet
  facet normal 0.319303 0.947653 0.000000
    outer loop
      vertex 25.162329 -0.161221 -4.500000
      vertex 25.290590 -0.204437 -4.500000
      vertex 25.290590 -0.204437 -6.500000
    endloop
  endfacet
  facet normal 0.319303 0.947653 0.000000
    outer loop
      vertex 25.162329 -0.161221 -4.500000
      vertex 25.290590 -0.204437 -6.500000
      vertex 25.162329 -0.161221 -6.500000
    endloop
  endfacet
  facet normal 0.419886 0.907577 0.000000
    outer loop
      vertex 25.039490 -0.104390 -4.500000
      vertex 25.162329 -0.161221 -4.500000
      vertex 25.162329 -0.161221 -6.500000
    endloop
  endfacet
  facet normal 0.419886 0.907577 0.000000
    outer loop
      vertex 25.039490 -0.104390 -4.500000
      vertex 25.162329 -0.161221 -6.500000
      vertex 25.039490 -0.104390 -6.500000
    endloop
  endfacet
  facet normal 0.515556 0.856856 0.000000
    outer loop
      vertex 24.923517 -0.034611 -4.500000
      vertex 25.039490 -0.104390 -4.500000
      vertex 25.039490 -0.104390 -6.500000
    endloop
  endfacet
  facet normal 0.515556 0.856856 0.000000
    outer loop
      vertex 24.923517 -0.034611 -4.500000
      vertex 25.039490 -0.104390 -6.500000
      vertex 24.923517 -0.034611 -6.500000
    endloop
  endfacet
  facet normal 0.605171 0.796095 0.000000
    outer loop
      vertex 24.815767 0.047297 -4.500000
      vertex 24.923517 -0.034611 -4.500000
      vertex 24.923517 -0.034611 -6.500000
    endloop
  endfacet
  facet normal 0.605171 0.796095 0.000000
    outer loop
      vertex 24.815767 0.047297 -4.500000
      vertex 24.923517 -0.034611 -6.500000
      vertex 24.815767 0.047297 -6.500000
    endloop
  endfacet
  facet normal 0.687702 0.725993 0.000000
    outer loop
      vertex 24.717506 0.140376 -4.500000
      vertex 24.815767 0.047297 -4.500000
      vertex 24.815767 0.047297 -6.500000
    endloop
  endfacet
  facet normal 0.687702 0.725993 0.000000
    outer loop
      vertex 24.717506 0.140376 -4.500000
      vertex 24.815767 0.047297 -6.500000
      vertex 24.717506 0.140376 -6.500000
    endloop
  endfacet
  facet normal 0.762156 0.647393 0.000000
    outer loop
      vertex 24.629883 0.243532 -4.500000
      vertex 24.717506 0.140376 -4.500000
      vertex 24.717506 0.140376 -6.500000
    endloop
  endfacet
  facet normal 0.762156 0.647393 0.000000
    outer loop
      vertex 24.629883 0.243532 -4.500000
      vertex 24.717506 0.140376 -6.500000
      vertex 24.629883 0.243532 -6.500000
    endloop
  endfacet
  facet normal 0.827691 0.561183 0.000000
    outer loop
      vertex 24.553928 0.355558 -4.500000
      vertex 24.629883 0.243532 -4.500000
      vertex 24.629883 0.243532 -6.500000
    endloop
  endfacet
  facet normal 0.827691 0.561183 0.000000
    outer loop
      vertex 24.553928 0.355558 -4.500000
      vertex 24.629883 0.243532 -6.500000
      vertex 24.553928 0.355558 -6.500000
    endloop
  endfacet
  facet normal 0.883516 0.468401 0.000000
    outer loop
      vertex 24.490532 0.475139 -4.500000
      vertex 24.553928 0.355558 -4.500000
      vertex 24.553928 0.355558 -6.500000
    endloop
  endfacet
  facet normal 0.883516 0.468401 0.000000
    outer loop
      vertex 24.490532 0.475139 -4.500000
      vertex 24.553928 0.355558 -6.500000
      vertex 24.490532 0.475139 -6.500000
    endloop
  endfacet
  facet normal 0.928974 0.370146 0.000000
    outer loop
      vertex 24.440434 0.600873 -4.500000
      vertex 24.490532 0.475139 -4.500000
      vertex 24.490532 0.475139 -6.500000
    endloop
  endfacet
  facet normal 0.928974 0.370146 0.000000
    outer loop
      vertex 24.440434 0.600873 -4.500000
      vertex 24.490532 0.475139 -6.500000
      vertex 24.440434 0.600873 -6.500000
    endloop
  endfacet
  facet normal 0.963550 0.267528 0.000000
    outer loop
      vertex 24.404224 0.731287 -4.500000
      vertex 24.440434 0.600873 -4.500000
      vertex 24.440434 0.600873 -6.500000
    endloop
  endfacet
  facet normal 0.963550 0.267528 0.000000
    outer loop
      vertex 24.404224 0.731287 -4.500000
      vertex 24.440434 0.600873 -6.500000
      vertex 24.404224 0.731287 -6.500000
    endloop
  endfacet
  facet normal 0.986825 0.161793 0.000000
    outer loop
      vertex 24.382326 0.864851 -4.500000
      vertex 24.404224 0.731287 -4.500000
      vertex 24.404224 0.731287 -6.500000
    endloop
  endfacet
  facet normal 0.986825 0.161793 0.000000
    outer loop
      vertex 24.382326 0.864851 -4.500000
      vertex 24.404224 0.731287 -6.500000
      vertex 24.382326 0.864851 -6.500000
    endloop
  endfacet
  facet normal 0.998534 0.054128 0.000000
    outer loop
      vertex 24.375000 1.000000 -4.500000
      vertex 24.382326 0.864851 -4.500000
      vertex 24.382326 0.864851 -6.500000
    endloop
  endfacet
  facet normal 0.998534 0.054128 0.000000
    outer loop
      vertex 24.375000 1.000000 -4.500000
      vertex 24.382326 0.864851 -6.500000
      vertex 24.375000 1.000000 -6.500000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 28.000000 3.000000 -4.500000
      vertex 28.000000 3.000000 -6.500000
      vertex 23.250000 3.000000 -6.500000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 28.000000 3.000000 -4.500000
      vertex 23.250000 3.000000 -6.500000
      vertex 23.250000 3.000000 -4.500000
    endloop
  endfacet
  facet normal -1.000000 0.000000 0.000000
    outer loop
      vertex 23.250000 -1.000000 -4.500000
      vertex 23.250000 3.000000 -4.500000
      vertex 23.250000 3.000000 -6.500000
    endloop
  endfacet
  facet normal -1.000000 0.000000 0.000000
    outer loop
      vertex 23.250000 -1.000000 -4.500000
      vertex 23.250000 3.000000 -6.500000
      vertex 23.250000 -1.000000 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 28.000000 0.000000 -6.500000
      vertex 26.809566 0.600873 -6.500000
      vertex 26.845776 0.731287 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 28.000000 0.000000 -6.500000
      vertex 26.845776 0.731287 -6.500000
      vertex 26.867672 0.864851 -6.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 24.440434 0.600873 -6.500000
      vertex 23.250000 -1.000000 -6.500000
      vertex 24.404224 0.731287 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 28.000000 0.000000 -6.500000
      vertex 26.867672 0.864851 -6.500000
      vertex 26.875000 1.000000 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 28.000000 0.000000 -6.500000
      vertex 26.875000 1.000000 -6.500000
      vertex 26.867672 1.135149 -6.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 28.000000 3.000000 -6.500000
      vertex 28.000000 0.000000 -6.500000
      vertex 26.867672 1.135149 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 28.000000 3.000000 -6.500000
      vertex 26.867672 1.135149 -6.500000
      vertex 26.845776 1.268713 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 26.809566 1.399127 -6.500000
      vertex 28.000000 3.000000 -6.500000
      vertex 26.845776 1.268713 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 28.000000 3.000000 -6.500000
      vertex 26.809566 1.399127 -6.500000
      vertex 26.759470 1.524861 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 28.000000 3.000000 -6.500000
      vertex 26.759470 1.524861 -6.500000
      vertex 26.696072 1.644442 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 26.620115 1.756468 -6.500000
      vertex 28.000000 3.000000 -6.500000
      vertex 26.696072 1.644442 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.250000 3.000000 -6.500000
      vertex 24.553928 1.644442 -6.500000
      vertex 24.490532 1.524861 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.250000 3.000000 -6.500000
      vertex 24.490532 1.524861 -6.500000
      vertex 24.440434 1.399127 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 24.404224 1.268713 -6.500000
      vertex 23.250000 3.000000 -6.500000
      vertex 24.440434 1.399127 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.250000 3.000000 -6.500000
      vertex 24.404224 1.268713 -6.500000
      vertex 24.382326 1.135149 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.250000 3.000000 -6.500000
      vertex 24.382326 1.135149 -6.500000
      vertex 24.375000 1.000000 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.250000 -1.000000 -6.500000
      vertex 23.250000 3.000000 -6.500000
      vertex 24.375000 1.000000 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.250000 -1.000000 -6.500000
      vertex 24.375000 1.000000 -6.500000
      vertex 24.382326 0.864851 -6.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 24.404224 0.731287 -6.500000
      vertex 23.250000 -1.000000 -6.500000
      vertex 24.382326 0.864851 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 28.000000 -1.000000 -6.500000
      vertex 25.827227 -0.233533 -6.500000
      vertex 25.959410 -0.204437 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 28.000000 -1.000000 -6.500000
      vertex 25.959410 -0.204437 -6.500000
      vertex 26.087673 -0.161221 -6.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 26.210510 -0.104390 -6.500000
      vertex 28.000000 -1.000000 -6.500000
      vertex 26.087673 -0.161221 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 28.000000 -1.000000 -6.500000
      vertex 26.210510 -0.104390 -6.500000
      vertex 26.326483 -0.034611 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 28.000000 -1.000000 -6.500000
      vertex 26.326483 -0.034611 -6.500000
      vertex 26.434233 0.047297 -6.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 26.532494 0.140376 -6.500000
      vertex 28.000000 -1.000000 -6.500000
      vertex 26.434233 0.047297 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.250000 -1.000000 -6.500000
      vertex 24.440434 0.600873 -6.500000
      vertex 24.490532 0.475139 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.250000 -1.000000 -6.500000
      vertex 24.490532 0.475139 -6.500000
      vertex 24.553928 0.355558 -6.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 24.629883 0.243532 -6.500000
      vertex 23.250000 -1.000000 -6.500000
      vertex 24.553928 0.355558 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.250000 -1.000000 -6.500000
      vertex 24.629883 0.243532 -6.500000
      vertex 24.717506 0.140376 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.250000 -1.000000 -6.500000
      vertex 24.717506 0.140376 -6.500000
      vertex 24.815767 0.047297 -6.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 24.923517 -0.034611 -6.500000
      vertex 23.250000 -1.000000 -6.500000
      vertex 24.815767 0.047297 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 28.000000 -1.000000 -6.500000
      vertex 26.532494 0.140376 -6.500000
      vertex 26.620115 0.243532 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 28.000000 -1.000000 -6.500000
      vertex 26.620115 0.243532 -6.500000
      vertex 26.696072 0.355558 -6.500000
    endloop
  endfacet
  facet normal -0.000000 -0.000000 -1.000000
    outer loop
      vertex 28.000000 0.000000 -6.500000
      vertex 28.000000 -1.000000 -6.500000
      vertex 26.696072 0.355558 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 28.000000 0.000000 -6.500000
      vertex 26.696072 0.355558 -6.500000
      vertex 26.759470 0.475139 -6.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 26.809566 0.600873 -6.500000
      vertex 28.000000 0.000000 -6.500000
      vertex 26.759470 0.475139 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 28.000000 3.000000 -6.500000
      vertex 26.620115 1.756468 -6.500000
      vertex 26.532494 1.859624 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 28.000000 3.000000 -6.500000
      vertex 26.532494 1.859624 -6.500000
      vertex 26.434233 1.952703 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 26.326483 2.034611 -6.500000
      vertex 28.000000 3.000000 -6.500000
      vertex 26.434233 1.952703 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.250000 3.000000 -6.500000
      vertex 24.923517 2.034611 -6.500000
      vertex 24.815767 1.952703 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.250000 -1.000000 -6.500000
      vertex 24.923517 -0.034611 -6.500000
      vertex 25.039490 -0.104390 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.250000 -1.000000 -6.500000
      vertex 25.039490 -0.104390 -6.500000
      vertex 25.162329 -0.161221 -6.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 25.290590 -0.204437 -6.500000
      vertex 23.250000 -1.000000 -6.500000
      vertex 25.162329 -0.161221 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.250000 3.000000 -6.500000
      vertex 24.815767 1.952703 -6.500000
      vertex 24.717506 1.859624 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.250000 3.000000 -6.500000
      vertex 24.717506 1.859624 -6.500000
      vertex 24.629883 1.756468 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 24.553928 1.644442 -6.500000
      vertex 23.250000 3.000000 -6.500000
      vertex 24.629883 1.756468 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.250000 -1.000000 -6.500000
      vertex 25.290590 -0.204437 -6.500000
      vertex 25.422771 -0.233533 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.250000 -1.000000 -6.500000
      vertex 25.422771 -0.233533 -6.500000
      vertex 25.557325 -0.248167 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 28.000000 -1.000000 -6.500000
      vertex 23.250000 -1.000000 -6.500000
      vertex 25.557325 -0.248167 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 28.000000 -1.000000 -6.500000
      vertex 25.557325 -0.248167 -6.500000
      vertex 25.692673 -0.248167 -6.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 25.827227 -0.233533 -6.500000
      vertex 28.000000 -1.000000 -6.500000
      vertex 25.692673 -0.248167 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 28.000000 3.000000 -6.500000
      vertex 26.326483 2.034611 -6.500000
      vertex 26.210510 2.104390 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 28.000000 3.000000 -6.500000
      vertex 26.210510 2.104390 -6.500000
      vertex 26.087673 2.161221 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 25.959410 2.204437 -6.500000
      vertex 28.000000 3.000000 -6.500000
      vertex 26.087673 2.161221 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 25.290590 2.204437 -6.500000
      vertex 23.250000 3.000000 -6.500000
      vertex 25.422771 2.233533 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.250000 3.000000 -6.500000
      vertex 25.290590 2.204437 -6.500000
      vertex 25.162329 2.161221 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.250000 3.000000 -6.500000
      vertex 25.162329 2.161221 -6.500000
      vertex 25.039490 2.104390 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 24.923517 2.034611 -6.500000
      vertex 23.250000 3.000000 -6.500000
      vertex 25.039490 2.104390 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 28.000000 3.000000 -6.500000
      vertex 25.959410 2.204437 -6.500000
      vertex 25.827227 2.233533 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 28.000000 3.000000 -6.500000
      vertex 25.827227 2.233533 -6.500000
      vertex 25.692673 2.248167 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.250000 3.000000 -6.500000
      vertex 28.000000 3.000000 -6.500000
      vertex 25.692673 2.248167 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.250000 3.000000 -6.500000
      vertex 25.692673 2.248167 -6.500000
      vertex 25.557325 2.248167 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 25.422771 2.233533 -6.500000
      vertex 23.250000 3.000000 -6.500000
      vertex 25.557325 2.248167 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 28.000000 3.000000 -4.500000
      vertex 26.696072 1.644442 -4.500000
      vertex 26.759470 1.524861 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 26.867672 0.864851 -4.500000
      vertex 26.845776 0.731287 -4.500000
      vertex 28.000000 0.000000 -4.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 26.867672 0.864851 -4.500000
      vertex 28.000000 0.000000 -4.500000
      vertex 26.875000 1.000000 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.250000 -1.000000 -4.500000
      vertex 24.440434 0.600873 -4.500000
      vertex 24.404224 0.731287 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 24.440434 1.399127 -4.500000
      vertex 23.250000 3.000000 -4.500000
      vertex 24.404224 1.268713 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 28.000000 3.000000 -4.500000
      vertex 26.759470 1.524861 -4.500000
      vertex 26.809566 1.399127 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 28.000000 3.000000 -4.500000
      vertex 26.809566 1.399127 -4.500000
      vertex 26.845776 1.268713 -4.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 28.000000 0.000000 -4.500000
      vertex 28.000000 3.000000 -4.500000
      vertex 26.845776 1.268713 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 28.000000 0.000000 -4.500000
      vertex 26.845776 1.268713 -4.500000
      vertex 26.867672 1.135149 -4.500000
    endloop
  endfacet
  facet normal -0.000000 -0.000000 1.000000
    outer loop
      vertex 26.875000 1.000000 -4.500000
      vertex 28.000000 0.000000 -4.500000
      vertex 26.867672 1.135149 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.250000 -1.000000 -4.500000
      vertex 24.404224 0.731287 -4.500000
      vertex 24.382326 0.864851 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.250000 -1.000000 -4.500000
      vertex 24.382326 0.864851 -4.500000
      vertex 24.375000 1.000000 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.250000 3.000000 -4.500000
      vertex 23.250000 -1.000000 -4.500000
      vertex 24.375000 1.000000 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.250000 3.000000 -4.500000
      vertex 24.375000 1.000000 -4.500000
      vertex 24.382326 1.135149 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 24.404224 1.268713 -4.500000
      vertex 23.250000 3.000000 -4.500000
      vertex 24.382326 1.135149 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.250000 3.000000 -4.500000
      vertex 24.440434 1.399127 -4.500000
      vertex 24.490532 1.524861 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.250000 3.000000 -4.500000
      vertex 24.490532 1.524861 -4.500000
      vertex 24.553928 1.644442 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 24.629883 1.756468 -4.500000
      vertex 23.250000 3.000000 -4.500000
      vertex 24.553928 1.644442 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 28.000000 3.000000 -4.500000
      vertex 26.326483 2.034611 -4.500000
      vertex 26.434233 1.952703 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 28.000000 -1.000000 -4.500000
      vertex 26.620115 0.243532 -4.500000
      vertex 26.532494 0.140376 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 28.000000 -1.000000 -4.500000
      vertex 26.532494 0.140376 -4.500000
      vertex 26.434233 0.047297 -4.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 26.326483 -0.034611 -4.500000
      vertex 28.000000 -1.000000 -4.500000
      vertex 26.434233 0.047297 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 28.000000 -1.000000 -4.500000
      vertex 26.326483 -0.034611 -4.500000
      vertex 26.210510 -0.104390 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 28.000000 -1.000000 -4.500000
      vertex 26.210510 -0.104390 -4.500000
      vertex 26.087673 -0.161221 -4.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 25.959410 -0.204437 -4.500000
      vertex 28.000000 -1.000000 -4.500000
      vertex 26.087673 -0.161221 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 28.000000 3.000000 -4.500000
      vertex 26.434233 1.952703 -4.500000
      vertex 26.532494 1.859624 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 28.000000 3.000000 -4.500000
      vertex 26.532494 1.859624 -4.500000
      vertex 26.620115 1.756468 -4.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 26.696072 1.644442 -4.500000
      vertex 28.000000 3.000000 -4.500000
      vertex 26.620115 1.756468 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 28.000000 0.000000 -4.500000
      vertex 26.845776 0.731287 -4.500000
      vertex 26.809566 0.600873 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 28.000000 0.000000 -4.500000
      vertex 26.809566 0.600873 -4.500000
      vertex 26.759470 0.475139 -4.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 28.000000 -1.000000 -4.500000
      vertex 28.000000 0.000000 -4.500000
      vertex 26.759470 0.475139 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 28.000000 -1.000000 -4.500000
      vertex 26.759470 0.475139 -4.500000
      vertex 26.696072 0.355558 -4.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 26.620115 0.243532 -4.500000
      vertex 28.000000 -1.000000 -4.500000
      vertex 26.696072 0.355558 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 25.290590 -0.204437 -4.500000
      vertex 23.250000 -1.000000 -4.500000
      vertex 25.422771 -0.233533 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.250000 -1.000000 -4.500000
      vertex 24.923517 -0.034611 -4.500000
      vertex 24.815767 0.047297 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.250000 -1.000000 -4.500000
      vertex 24.815767 0.047297 -4.500000
      vertex 24.717506 0.140376 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 24.629883 0.243532 -4.500000
      vertex 23.250000 -1.000000 -4.500000
      vertex 24.717506 0.140376 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.250000 -1.000000 -4.500000
      vertex 24.629883 0.243532 -4.500000
      vertex 24.553928 0.355558 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.250000 -1.000000 -4.500000
      vertex 24.553928 0.355558 -4.500000
      vertex 24.490532 0.475139 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 24.440434 0.600873 -4.500000
      vertex 23.250000 -1.000000 -4.500000
      vertex 24.490532 0.475139 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.250000 -1.000000 -4.500000
      vertex 25.290590 -0.204437 -4.500000
      vertex 25.162329 -0.161221 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.250000 -1.000000 -4.500000
      vertex 25.162329 -0.161221 -4.500000
      vertex 25.039490 -0.104390 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 24.923517 -0.034611 -4.500000
      vertex 23.250000 -1.000000 -4.500000
      vertex 25.039490 -0.104390 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 28.000000 -1.000000 -4.500000
      vertex 25.959410 -0.204437 -4.500000
      vertex 25.827227 -0.233533 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 28.000000 -1.000000 -4.500000
      vertex 25.827227 -0.233533 -4.500000
      vertex 25.692673 -0.248167 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.250000 -1.000000 -4.500000
      vertex 28.000000 -1.000000 -4.500000
      vertex 25.692673 -0.248167 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.250000 -1.000000 -4.500000
      vertex 25.692673 -0.248167 -4.500000
      vertex 25.557325 -0.248167 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 25.422771 -0.233533 -4.500000
      vertex 23.250000 -1.000000 -4.500000
      vertex 25.557325 -0.248167 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.250000 3.000000 -4.500000
      vertex 24.629883 1.756468 -4.500000
      vertex 24.717506 1.859624 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.250000 3.000000 -4.500000
      vertex 24.717506 1.859624 -4.500000
      vertex 24.815767 1.952703 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 24.923517 2.034611 -4.500000
      vertex 23.250000 3.000000 -4.500000
      vertex 24.815767 1.952703 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.250000 3.000000 -4.500000
      vertex 24.923517 2.034611 -4.500000
      vertex 25.039490 2.104390 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.250000 3.000000 -4.500000
      vertex 25.039490 2.104390 -4.500000
      vertex 25.162329 2.161221 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 25.290590 2.204437 -4.500000
      vertex 23.250000 3.000000 -4.500000
      vertex 25.162329 2.161221 -4.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 25.959410 2.204437 -4.500000
      vertex 28.000000 3.000000 -4.500000
      vertex 25.827227 2.233533 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 28.000000 3.000000 -4.500000
      vertex 25.959410 2.204437 -4.500000
      vertex 26.087673 2.161221 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 28.000000 3.000000 -4.500000
      vertex 26.087673 2.161221 -4.500000
      vertex 26.210510 2.104390 -4.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 26.326483 2.034611 -4.500000
      vertex 28.000000 3.000000 -4.500000
      vertex 26.210510 2.104390 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.250000 3.000000 -4.500000
      vertex 25.290590 2.204437 -4.500000
      vertex 25.422771 2.233533 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.250000 3.000000 -4.500000
      vertex 25.422771 2.233533 -4.500000
      vertex 25.557325 2.248167 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 28.000000 3.000000 -4.500000
      vertex 23.250000 3.000000 -4.500000
      vertex 25.557325 2.248167 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 28.000000 3.000000 -4.500000
      vertex 25.557325 2.248167 -4.500000
      vertex 25.692673 2.248167 -4.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 25.827227 2.233533 -4.500000
      vertex 28.000000 3.000000 -4.500000
      vertex 25.692673 2.248167 -4.500000
    endloop
  endfacet
  facet normal -0.000000 1.000000 0.000000
    outer loop
      vertex 3.000000 3.000000 -4.500000
      vertex 7.750000 3.000000 -4.500000
      vertex 7.750000 3.000000 -6.500000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 3.000000 3.000000 -4.500000
      vertex 7.750000 3.000000 -6.500000
      vertex 3.000000 3.000000 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.000000 0.000000 -6.500000
      vertex 4.125000 1.000000 -6.500000
      vertex 4.132328 0.864851 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.000000 0.000000 -6.500000
      vertex 4.132328 0.864851 -6.500000
      vertex 4.154224 0.731287 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 7.750000 -1.000000 -6.500000
      vertex 6.282495 0.140376 -6.500000
      vertex 6.370117 0.243532 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.000000 0.000000 -6.500000
      vertex 4.154224 0.731287 -6.500000
      vertex 4.190434 0.600873 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.000000 0.000000 -6.500000
      vertex 4.190434 0.600873 -6.500000
      vertex 4.240530 0.475139 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.000000 -1.000000 -6.500000
      vertex 3.000000 0.000000 -6.500000
      vertex 4.240530 0.475139 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.000000 -1.000000 -6.500000
      vertex 4.240530 0.475139 -6.500000
      vertex 4.303928 0.355558 -6.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 4.379884 0.243532 -6.500000
      vertex 3.000000 -1.000000 -6.500000
      vertex 4.303928 0.355558 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 7.750000 3.000000 -6.500000
      vertex 6.076484 2.034611 -6.500000
      vertex 5.960511 2.104390 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 7.750000 3.000000 -6.500000
      vertex 5.960511 2.104390 -6.500000
      vertex 5.837673 2.161221 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 5.709411 2.204437 -6.500000
      vertex 7.750000 3.000000 -6.500000
      vertex 5.837673 2.161221 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 5.040590 2.204437 -6.500000
      vertex 3.000000 3.000000 -6.500000
      vertex 5.172772 2.233533 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.000000 3.000000 -6.500000
      vertex 4.673516 2.034611 -6.500000
      vertex 4.565767 1.952703 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.000000 3.000000 -6.500000
      vertex 4.565767 1.952703 -6.500000
      vertex 4.467505 1.859624 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.000000 3.000000 -6.500000
      vertex 4.467505 1.859624 -6.500000
      vertex 4.379884 1.756468 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.000000 3.000000 -6.500000
      vertex 4.379884 1.756468 -6.500000
      vertex 4.303928 1.644442 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 4.240530 1.524861 -6.500000
      vertex 3.000000 3.000000 -6.500000
      vertex 4.303928 1.644442 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 7.750000 3.000000 -6.500000
      vertex 5.709411 2.204437 -6.500000
      vertex 5.577228 2.233533 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 7.750000 3.000000 -6.500000
      vertex 5.577228 2.233533 -6.500000
      vertex 5.442674 2.248167 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.000000 3.000000 -6.500000
      vertex 7.750000 3.000000 -6.500000
      vertex 5.442674 2.248167 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.000000 3.000000 -6.500000
      vertex 5.442674 2.248167 -6.500000
      vertex 5.307327 2.248167 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 5.172772 2.233533 -6.500000
      vertex 3.000000 3.000000 -6.500000
      vertex 5.307327 2.248167 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.000000 3.000000 -6.500000
      vertex 5.040590 2.204437 -6.500000
      vertex 4.912327 2.161221 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.000000 3.000000 -6.500000
      vertex 4.912327 2.161221 -6.500000
      vertex 4.789489 2.104390 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 4.673516 2.034611 -6.500000
      vertex 3.000000 3.000000 -6.500000
      vertex 4.789489 2.104390 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.000000 -1.000000 -6.500000
      vertex 4.379884 0.243532 -6.500000
      vertex 4.467505 0.140376 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.000000 -1.000000 -6.500000
      vertex 4.467505 0.140376 -6.500000
      vertex 4.565767 0.047297 -6.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 4.673516 -0.034611 -6.500000
      vertex 3.000000 -1.000000 -6.500000
      vertex 4.565767 0.047297 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 7.750000 -1.000000 -6.500000
      vertex 5.577228 -0.233533 -6.500000
      vertex 5.709411 -0.204437 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 7.750000 -1.000000 -6.500000
      vertex 5.709411 -0.204437 -6.500000
      vertex 5.837673 -0.161221 -6.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 5.960511 -0.104390 -6.500000
      vertex 7.750000 -1.000000 -6.500000
      vertex 5.837673 -0.161221 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 7.750000 -1.000000 -6.500000
      vertex 5.960511 -0.104390 -6.500000
      vertex 6.076484 -0.034611 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 7.750000 -1.000000 -6.500000
      vertex 6.076484 -0.034611 -6.500000
      vertex 6.184233 0.047297 -6.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 6.282495 0.140376 -6.500000
      vertex 7.750000 -1.000000 -6.500000
      vertex 6.184233 0.047297 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 7.750000 -1.000000 -6.500000
      vertex 6.370117 0.243532 -6.500000
      vertex 6.446072 0.355558 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 7.750000 -1.000000 -6.500000
      vertex 6.446072 0.355558 -6.500000
      vertex 6.509470 0.475139 -6.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 6.559566 0.600873 -6.500000
      vertex 7.750000 -1.000000 -6.500000
      vertex 6.509470 0.475139 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 7.750000 -1.000000 -6.500000
      vertex 6.559566 0.600873 -6.500000
      vertex 6.595776 0.731287 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 7.750000 -1.000000 -6.500000
      vertex 6.595776 0.731287 -6.500000
      vertex 6.617672 0.864851 -6.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 7.750000 3.000000 -6.500000
      vertex 7.750000 -1.000000 -6.500000
      vertex 6.617672 0.864851 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 7.750000 3.000000 -6.500000
      vertex 6.617672 0.864851 -6.500000
      vertex 6.625000 1.000000 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 7.750000 3.000000 -6.500000
      vertex 6.370117 1.756468 -6.500000
      vertex 6.282495 1.859624 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 7.750000 3.000000 -6.500000
      vertex 6.282495 1.859624 -6.500000
      vertex 6.184233 1.952703 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 6.076484 2.034611 -6.500000
      vertex 7.750000 3.000000 -6.500000
      vertex 6.184233 1.952703 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.000000 3.000000 -6.500000
      vertex 4.240530 1.524861 -6.500000
      vertex 4.190434 1.399127 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.000000 3.000000 -6.500000
      vertex 4.190434 1.399127 -6.500000
      vertex 4.154224 1.268713 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.000000 0.000000 -6.500000
      vertex 3.000000 3.000000 -6.500000
      vertex 4.154224 1.268713 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.000000 0.000000 -6.500000
      vertex 4.154224 1.268713 -6.500000
      vertex 4.132328 1.135149 -6.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 4.125000 1.000000 -6.500000
      vertex 3.000000 0.000000 -6.500000
      vertex 4.132328 1.135149 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 7.750000 3.000000 -6.500000
      vertex 6.625000 1.000000 -6.500000
      vertex 6.617672 1.135149 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 7.750000 3.000000 -6.500000
      vertex 6.617672 1.135149 -6.500000
      vertex 6.595776 1.268713 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 6.559566 1.399127 -6.500000
      vertex 7.750000 3.000000 -6.500000
      vertex 6.595776 1.268713 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.000000 -1.000000 -6.500000
      vertex 4.673516 -0.034611 -6.500000
      vertex 4.789489 -0.104390 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.000000 -1.000000 -6.500000
      vertex 4.789489 -0.104390 -6.500000
      vertex 4.912327 -0.161221 -6.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 5.040590 -0.204437 -6.500000
      vertex 3.000000 -1.000000 -6.500000
      vertex 4.912327 -0.161221 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.000000 -1.000000 -6.500000
      vertex 5.040590 -0.204437 -6.500000
      vertex 5.172772 -0.233533 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.000000 -1.000000 -6.500000
      vertex 5.172772 -0.233533 -6.500000
      vertex 5.307327 -0.248167 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 7.750000 -1.000000 -6.500000
      vertex 3.000000 -1.000000 -6.500000
      vertex 5.307327 -0.248167 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 7.750000 -1.000000 -6.500000
      vertex 5.307327 -0.248167 -6.500000
      vertex 5.442674 -0.248167 -6.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 5.577228 -0.233533 -6.500000
      vertex 7.750000 -1.000000 -6.500000
      vertex 5.442674 -0.248167 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 7.750000 3.000000 -6.500000
      vertex 6.559566 1.399127 -6.500000
      vertex 6.509470 1.524861 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 7.750000 3.000000 -6.500000
      vertex 6.509470 1.524861 -6.500000
      vertex 6.446072 1.644442 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 6.370117 1.756468 -6.500000
      vertex 7.750000 3.000000 -6.500000
      vertex 6.446072 1.644442 -6.500000
    endloop
  endfacet
  facet normal 1.000000 0.000000 0.000000
    outer loop
      vertex 9.250000 -2.000000 -4.500000
      vertex 9.250000 -2.000000 -6.000000
      vertex 9.250000 -1.000000 -6.000000
    endloop
  endfacet
  facet normal 1.000000 -0.000000 0.000000
    outer loop
      vertex 9.250000 -2.000000 -4.500000
      vertex 9.250000 -1.000000 -6.000000
      vertex 9.250000 -1.000000 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.500000 8.000000 20.500000
      vertex -1.500000 14.000000 20.500000
      vertex 0.000000 14.000000 20.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.500000 8.000000 20.500000
      vertex 0.000000 14.000000 20.500000
      vertex 0.000000 8.000000 20.500000
    endloop
  endfacet
  facet normal -0.000000 1.000000 0.000000
    outer loop
      vertex 0.000000 39.500000 2.000000
      vertex 2.000000 39.500000 2.000000
      vertex 2.000000 39.500000 0.000000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 0.000000 39.500000 2.000000
      vertex 2.000000 39.500000 0.000000
      vertex 0.000000 39.500000 0.000000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 -0.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex -0.000000 71.000000 2.000000
      vertex 2.000000 71.000000 11.000000
    endloop
  endfacet
  facet normal -0.000000 -1.000000 0.000000
    outer loop
      vertex 23.000000 71.000000 11.000000
      vertex 2.000000 71.000000 11.000000
      vertex -0.000000 71.000000 2.000000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 -0.000000
    outer loop
      vertex 23.000000 71.000000 11.000000
      vertex -0.000000 71.000000 2.000000
      vertex 31.000000 71.000000 2.000000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 0.000000
    outer loop
      vertex 23.000000 71.000000 13.000000
      vertex 23.000000 71.000000 11.000000
      vertex 31.000000 71.000000 2.000000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 0.000000
    outer loop
      vertex 23.000000 71.000000 13.000000
      vertex 31.000000 71.000000 2.000000
      vertex 31.000000 71.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 0.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex 23.000000 71.000000 13.000000
      vertex 31.000000 71.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 0.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex 31.000000 71.000000 23.000000
      vertex -0.000000 71.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 0.000000
    outer loop
      vertex -0.000000 71.000000 2.000000
      vertex 2.000000 71.000000 13.000000
      vertex -0.000000 71.000000 23.000000
    endloop
  endfacet
  facet normal -0.998533 -0.054143 0.000000
    outer loop
      vertex 5.892965 67.429741 11.000000
      vertex 5.900000 67.300003 11.000000
      vertex 5.900000 67.300003 13.000000
    endloop
  endfacet
  facet normal -0.998533 -0.054143 0.000000
    outer loop
      vertex 5.892965 67.429741 11.000000
      vertex 5.900000 67.300003 13.000000
      vertex 5.892965 67.429741 13.000000
    endloop
  endfacet
  facet normal -0.986828 -0.161775 0.000000
    outer loop
      vertex 5.871944 67.557968 11.000000
      vertex 5.892965 67.429741 11.000000
      vertex 5.892965 67.429741 13.000000
    endloop
  endfacet
  facet normal -0.986828 -0.161775 0.000000
    outer loop
      vertex 5.871944 67.557968 11.000000
      vertex 5.892965 67.429741 13.000000
      vertex 5.871944 67.557968 13.000000
    endloop
  endfacet
  facet normal -0.963547 -0.267539 0.000000
    outer loop
      vertex 5.837184 67.683159 11.000000
      vertex 5.871944 67.557968 11.000000
      vertex 5.871944 67.557968 13.000000
    endloop
  endfacet
  facet normal -0.963547 -0.267539 0.000000
    outer loop
      vertex 5.837184 67.683159 11.000000
      vertex 5.871944 67.557968 13.000000
      vertex 5.837184 67.683159 13.000000
    endloop
  endfacet
  facet normal -0.928976 -0.370139 0.000000
    outer loop
      vertex 5.789091 67.803864 11.000000
      vertex 5.837184 67.683159 11.000000
      vertex 5.837184 67.683159 13.000000
    endloop
  endfacet
  facet normal -0.928976 -0.370139 0.000000
    outer loop
      vertex 5.789091 67.803864 11.000000
      vertex 5.837184 67.683159 13.000000
      vertex 5.789091 67.803864 13.000000
    endloop
  endfacet
  facet normal -0.883515 -0.468404 0.000000
    outer loop
      vertex 5.728229 67.918663 11.000000
      vertex 5.789091 67.803864 11.000000
      vertex 5.789091 67.803864 13.000000
    endloop
  endfacet
  facet normal -0.883515 -0.468404 0.000000
    outer loop
      vertex 5.728229 67.918663 11.000000
      vertex 5.789091 67.803864 13.000000
      vertex 5.728229 67.918663 13.000000
    endloop
  endfacet
  facet normal -0.827688 -0.561189 0.000000
    outer loop
      vertex 5.655312 68.026207 11.000000
      vertex 5.728229 67.918663 11.000000
      vertex 5.728229 67.918663 13.000000
    endloop
  endfacet
  facet normal -0.827688 -0.561189 0.000000
    outer loop
      vertex 5.655312 68.026207 11.000000
      vertex 5.728229 67.918663 13.000000
      vertex 5.655312 68.026207 13.000000
    endloop
  endfacet
  facet normal -0.762185 -0.647359 0.000000
    outer loop
      vertex 5.571195 68.125244 11.000000
      vertex 5.655312 68.026207 11.000000
      vertex 5.655312 68.026207 13.000000
    endloop
  endfacet
  facet normal -0.762185 -0.647359 0.000000
    outer loop
      vertex 5.571195 68.125244 11.000000
      vertex 5.655312 68.026207 13.000000
      vertex 5.571195 68.125244 13.000000
    endloop
  endfacet
  facet normal -0.687669 -0.726024 0.000000
    outer loop
      vertex 5.476863 68.214592 11.000000
      vertex 5.571195 68.125244 11.000000
      vertex 5.571195 68.125244 13.000000
    endloop
  endfacet
  facet normal -0.687669 -0.726024 0.000000
    outer loop
      vertex 5.476863 68.214592 11.000000
      vertex 5.571195 68.125244 13.000000
      vertex 5.476863 68.214592 13.000000
    endloop
  endfacet
  facet normal -0.605194 -0.796078 0.000000
    outer loop
      vertex 5.373425 68.293228 11.000000
      vertex 5.476863 68.214592 11.000000
      vertex 5.476863 68.214592 13.000000
    endloop
  endfacet
  facet normal -0.605194 -0.796078 0.000000
    outer loop
      vertex 5.373425 68.293228 11.000000
      vertex 5.476863 68.214592 13.000000
      vertex 5.373425 68.293228 13.000000
    endloop
  endfacet
  facet normal -0.515545 -0.856862 0.000000
    outer loop
      vertex 5.262090 68.360214 11.000000
      vertex 5.373425 68.293228 11.000000
      vertex 5.373425 68.293228 13.000000
    endloop
  endfacet
  facet normal -0.515545 -0.856862 0.000000
    outer loop
      vertex 5.262090 68.360214 11.000000
      vertex 5.373425 68.293228 13.000000
      vertex 5.262090 68.360214 13.000000
    endloop
  endfacet
  facet normal -0.419891 -0.907575 0.000000
    outer loop
      vertex 5.144166 68.414772 11.000000
      vertex 5.262090 68.360214 11.000000
      vertex 5.262090 68.360214 13.000000
    endloop
  endfacet
  facet normal -0.419891 -0.907575 0.000000
    outer loop
      vertex 5.144166 68.414772 11.000000
      vertex 5.262090 68.360214 13.000000
      vertex 5.144166 68.414772 13.000000
    endloop
  endfacet
  facet normal -0.319305 -0.947652 0.000000
    outer loop
      vertex 5.021034 68.456261 11.000000
      vertex 5.144166 68.414772 11.000000
      vertex 5.144166 68.414772 13.000000
    endloop
  endfacet
  facet normal -0.319305 -0.947652 0.000000
    outer loop
      vertex 5.021034 68.456261 11.000000
      vertex 5.144166 68.414772 13.000000
      vertex 5.021034 68.456261 13.000000
    endloop
  endfacet
  facet normal -0.214966 -0.976621 0.000000
    outer loop
      vertex 4.894138 68.484192 11.000000
      vertex 5.021034 68.456261 11.000000
      vertex 5.021034 68.456261 13.000000
    endloop
  endfacet
  facet normal -0.214966 -0.976621 0.000000
    outer loop
      vertex 4.894138 68.484192 11.000000
      vertex 5.021034 68.456261 13.000000
      vertex 4.894138 68.484192 13.000000
    endloop
  endfacet
  facet normal -0.108099 -0.994140 0.000000
    outer loop
      vertex 4.764966 68.498238 11.000000
      vertex 4.894138 68.484192 11.000000
      vertex 4.894138 68.484192 13.000000
    endloop
  endfacet
  facet normal -0.108099 -0.994140 0.000000
    outer loop
      vertex 4.764966 68.498238 11.000000
      vertex 4.894138 68.484192 13.000000
      vertex 4.764966 68.498238 13.000000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 0.000000
    outer loop
      vertex 4.635033 68.498238 11.000000
      vertex 4.764966 68.498238 11.000000
      vertex 4.764966 68.498238 13.000000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 0.000000
    outer loop
      vertex 4.635033 68.498238 11.000000
      vertex 4.764966 68.498238 13.000000
      vertex 4.635033 68.498238 13.000000
    endloop
  endfacet
  facet normal 0.108100 -0.994140 0.000000
    outer loop
      vertex 4.505862 68.484192 11.000000
      vertex 4.635033 68.498238 11.000000
      vertex 4.635033 68.498238 13.000000
    endloop
  endfacet
  facet normal 0.108100 -0.994140 0.000000
    outer loop
      vertex 4.505862 68.484192 11.000000
      vertex 4.635033 68.498238 13.000000
      vertex 4.505862 68.484192 13.000000
    endloop
  endfacet
  facet normal 0.214965 -0.976622 0.000000
    outer loop
      vertex 4.378966 68.456261 11.000000
      vertex 4.505862 68.484192 11.000000
      vertex 4.505862 68.484192 13.000000
    endloop
  endfacet
  facet normal 0.214965 -0.976622 0.000000
    outer loop
      vertex 4.378966 68.456261 11.000000
      vertex 4.505862 68.484192 13.000000
      vertex 4.378966 68.456261 13.000000
    endloop
  endfacet
  facet normal 0.319307 -0.947652 0.000000
    outer loop
      vertex 4.255834 68.414772 11.000000
      vertex 4.378966 68.456261 11.000000
      vertex 4.378966 68.456261 13.000000
    endloop
  endfacet
  facet normal 0.319307 -0.947652 0.000000
    outer loop
      vertex 4.255834 68.414772 11.000000
      vertex 4.378966 68.456261 13.000000
      vertex 4.255834 68.414772 13.000000
    endloop
  endfacet
  facet normal 0.419891 -0.907575 0.000000
    outer loop
      vertex 4.137910 68.360214 11.000000
      vertex 4.255834 68.414772 11.000000
      vertex 4.255834 68.414772 13.000000
    endloop
  endfacet
  facet normal 0.419891 -0.907575 0.000000
    outer loop
      vertex 4.137910 68.360214 11.000000
      vertex 4.255834 68.414772 13.000000
      vertex 4.137910 68.360214 13.000000
    endloop
  endfacet
  facet normal 0.515545 -0.856862 0.000000
    outer loop
      vertex 4.026576 68.293228 11.000000
      vertex 4.137910 68.360214 11.000000
      vertex 4.137910 68.360214 13.000000
    endloop
  endfacet
  facet normal 0.515545 -0.856862 0.000000
    outer loop
      vertex 4.026576 68.293228 11.000000
      vertex 4.137910 68.360214 13.000000
      vertex 4.026576 68.293228 13.000000
    endloop
  endfacet
  facet normal 0.605192 -0.796080 0.000000
    outer loop
      vertex 3.923136 68.214592 11.000000
      vertex 4.026576 68.293228 11.000000
      vertex 4.026576 68.293228 13.000000
    endloop
  endfacet
  facet normal 0.605192 -0.796080 0.000000
    outer loop
      vertex 3.923136 68.214592 11.000000
      vertex 4.026576 68.293228 13.000000
      vertex 3.923136 68.214592 13.000000
    endloop
  endfacet
  facet normal 0.687671 -0.726022 0.000000
    outer loop
      vertex 3.828805 68.125244 11.000000
      vertex 3.923136 68.214592 11.000000
      vertex 3.923136 68.214592 13.000000
    endloop
  endfacet
  facet normal 0.687671 -0.726022 0.000000
    outer loop
      vertex 3.828805 68.125244 11.000000
      vertex 3.923136 68.214592 13.000000
      vertex 3.828805 68.125244 13.000000
    endloop
  endfacet
  facet normal 0.762184 -0.647361 0.000000
    outer loop
      vertex 3.744688 68.026207 11.000000
      vertex 3.828805 68.125244 11.000000
      vertex 3.828805 68.125244 13.000000
    endloop
  endfacet
  facet normal 0.762184 -0.647361 0.000000
    outer loop
      vertex 3.744688 68.026207 11.000000
      vertex 3.828805 68.125244 13.000000
      vertex 3.744688 68.026207 13.000000
    endloop
  endfacet
  facet normal 0.827688 -0.561189 0.000000
    outer loop
      vertex 3.671771 67.918663 11.000000
      vertex 3.744688 68.026207 11.000000
      vertex 3.744688 68.026207 13.000000
    endloop
  endfacet
  facet normal 0.827688 -0.561189 0.000000
    outer loop
      vertex 3.671771 67.918663 11.000000
      vertex 3.744688 68.026207 13.000000
      vertex 3.671771 67.918663 13.000000
    endloop
  endfacet
  facet normal 0.883515 -0.468402 0.000000
    outer loop
      vertex 3.610909 67.803864 11.000000
      vertex 3.671771 67.918663 11.000000
      vertex 3.671771 67.918663 13.000000
    endloop
  endfacet
  facet normal 0.883515 -0.468402 0.000000
    outer loop
      vertex 3.610909 67.803864 11.000000
      vertex 3.671771 67.918663 13.000000
      vertex 3.610909 67.803864 13.000000
    endloop
  endfacet
  facet normal 0.928976 -0.370139 0.000000
    outer loop
      vertex 3.562816 67.683159 11.000000
      vertex 3.610909 67.803864 11.000000
      vertex 3.610909 67.803864 13.000000
    endloop
  endfacet
  facet normal 0.928976 -0.370139 0.000000
    outer loop
      vertex 3.562816 67.683159 11.000000
      vertex 3.610909 67.803864 13.000000
      vertex 3.562816 67.683159 13.000000
    endloop
  endfacet
  facet normal 0.963546 -0.267542 0.000000
    outer loop
      vertex 3.528055 67.557968 11.000000
      vertex 3.562816 67.683159 11.000000
      vertex 3.562816 67.683159 13.000000
    endloop
  endfacet
  facet normal 0.963546 -0.267542 0.000000
    outer loop
      vertex 3.528055 67.557968 11.000000
      vertex 3.562816 67.683159 13.000000
      vertex 3.528055 67.557968 13.000000
    endloop
  endfacet
  facet normal 0.986828 -0.161775 0.000000
    outer loop
      vertex 3.507034 67.429741 11.000000
      vertex 3.528055 67.557968 11.000000
      vertex 3.528055 67.557968 13.000000
    endloop
  endfacet
  facet normal 0.986828 -0.161775 0.000000
    outer loop
      vertex 3.507034 67.429741 11.000000
      vertex 3.528055 67.557968 13.000000
      vertex 3.507034 67.429741 13.000000
    endloop
  endfacet
  facet normal 0.998533 -0.054140 0.000000
    outer loop
      vertex 3.500000 67.300003 11.000000
      vertex 3.507034 67.429741 11.000000
      vertex 3.507034 67.429741 13.000000
    endloop
  endfacet
  facet normal 0.998533 -0.054140 0.000000
    outer loop
      vertex 3.500000 67.300003 11.000000
      vertex 3.507034 67.429741 13.000000
      vertex 3.500000 67.300003 13.000000
    endloop
  endfacet
  facet normal 0.998534 0.054137 0.000000
    outer loop
      vertex 3.507034 67.170258 11.000000
      vertex 3.500000 67.300003 11.000000
      vertex 3.500000 67.300003 13.000000
    endloop
  endfacet
  facet normal 0.998534 0.054137 -0.000000
    outer loop
      vertex 3.507034 67.170258 11.000000
      vertex 3.500000 67.300003 13.000000
      vertex 3.507034 67.170258 13.000000
    endloop
  endfacet
  facet normal 0.986826 0.161785 0.000000
    outer loop
      vertex 3.528055 67.042038 11.000000
      vertex 3.507034 67.170258 11.000000
      vertex 3.507034 67.170258 13.000000
    endloop
  endfacet
  facet normal 0.986826 0.161785 -0.000000
    outer loop
      vertex 3.528055 67.042038 11.000000
      vertex 3.507034 67.170258 13.000000
      vertex 3.528055 67.042038 13.000000
    endloop
  endfacet
  facet normal 0.963550 0.267527 0.000000
    outer loop
      vertex 3.562816 66.916840 11.000000
      vertex 3.528055 67.042038 11.000000
      vertex 3.528055 67.042038 13.000000
    endloop
  endfacet
  facet normal 0.963550 0.267527 -0.000000
    outer loop
      vertex 3.562816 66.916840 11.000000
      vertex 3.528055 67.042038 13.000000
      vertex 3.562816 66.916840 13.000000
    endloop
  endfacet
  facet normal 0.928976 0.370139 0.000000
    outer loop
      vertex 3.610909 66.796135 11.000000
      vertex 3.562816 66.916840 11.000000
      vertex 3.562816 66.916840 13.000000
    endloop
  endfacet
  facet normal 0.928976 0.370139 -0.000000
    outer loop
      vertex 3.610909 66.796135 11.000000
      vertex 3.562816 66.916840 13.000000
      vertex 3.610909 66.796135 13.000000
    endloop
  endfacet
  facet normal 0.883515 0.468402 0.000000
    outer loop
      vertex 3.671771 66.681335 11.000000
      vertex 3.610909 66.796135 11.000000
      vertex 3.610909 66.796135 13.000000
    endloop
  endfacet
  facet normal 0.883515 0.468402 -0.000000
    outer loop
      vertex 3.671771 66.681335 11.000000
      vertex 3.610909 66.796135 13.000000
      vertex 3.671771 66.681335 13.000000
    endloop
  endfacet
  facet normal 0.827688 0.561189 0.000000
    outer loop
      vertex 3.744688 66.573792 11.000000
      vertex 3.671771 66.681335 11.000000
      vertex 3.671771 66.681335 13.000000
    endloop
  endfacet
  facet normal 0.827688 0.561189 -0.000000
    outer loop
      vertex 3.744688 66.573792 11.000000
      vertex 3.671771 66.681335 13.000000
      vertex 3.744688 66.573792 13.000000
    endloop
  endfacet
  facet normal 0.762184 0.647361 0.000000
    outer loop
      vertex 3.828805 66.474754 11.000000
      vertex 3.744688 66.573792 11.000000
      vertex 3.744688 66.573792 13.000000
    endloop
  endfacet
  facet normal 0.762184 0.647361 -0.000000
    outer loop
      vertex 3.828805 66.474754 11.000000
      vertex 3.744688 66.573792 13.000000
      vertex 3.828805 66.474754 13.000000
    endloop
  endfacet
  facet normal 0.687671 0.726022 0.000000
    outer loop
      vertex 3.923136 66.385406 11.000000
      vertex 3.828805 66.474754 11.000000
      vertex 3.828805 66.474754 13.000000
    endloop
  endfacet
  facet normal 0.687671 0.726022 -0.000000
    outer loop
      vertex 3.923136 66.385406 11.000000
      vertex 3.828805 66.474754 13.000000
      vertex 3.923136 66.385406 13.000000
    endloop
  endfacet
  facet normal 0.605192 0.796080 0.000000
    outer loop
      vertex 4.026576 66.306770 11.000000
      vertex 3.923136 66.385406 11.000000
      vertex 3.923136 66.385406 13.000000
    endloop
  endfacet
  facet normal 0.605192 0.796080 -0.000000
    outer loop
      vertex 4.026576 66.306770 11.000000
      vertex 3.923136 66.385406 13.000000
      vertex 4.026576 66.306770 13.000000
    endloop
  endfacet
  facet normal 0.515502 0.856888 0.000000
    outer loop
      vertex 4.137910 66.239792 11.000000
      vertex 4.026576 66.306770 11.000000
      vertex 4.026576 66.306770 13.000000
    endloop
  endfacet
  facet normal 0.515502 0.856888 -0.000000
    outer loop
      vertex 4.137910 66.239792 11.000000
      vertex 4.026576 66.306770 13.000000
      vertex 4.137910 66.239792 13.000000
    endloop
  endfacet
  facet normal 0.419939 0.907552 0.000000
    outer loop
      vertex 4.255834 66.185226 11.000000
      vertex 4.137910 66.239792 11.000000
      vertex 4.137910 66.239792 13.000000
    endloop
  endfacet
  facet normal 0.419939 0.907552 -0.000000
    outer loop
      vertex 4.255834 66.185226 11.000000
      vertex 4.137910 66.239792 13.000000
      vertex 4.255834 66.185226 13.000000
    endloop
  endfacet
  facet normal 0.319254 0.947669 0.000000
    outer loop
      vertex 4.378966 66.143745 11.000000
      vertex 4.255834 66.185226 11.000000
      vertex 4.255834 66.185226 13.000000
    endloop
  endfacet
  facet normal 0.319254 0.947669 -0.000000
    outer loop
      vertex 4.378966 66.143745 11.000000
      vertex 4.255834 66.185226 13.000000
      vertex 4.378966 66.143745 13.000000
    endloop
  endfacet
  facet normal 0.214965 0.976622 0.000000
    outer loop
      vertex 4.505862 66.115814 11.000000
      vertex 4.378966 66.143745 11.000000
      vertex 4.378966 66.143745 13.000000
    endloop
  endfacet
  facet normal 0.214965 0.976622 -0.000000
    outer loop
      vertex 4.505862 66.115814 11.000000
      vertex 4.378966 66.143745 13.000000
      vertex 4.505862 66.115814 13.000000
    endloop
  endfacet
  facet normal 0.108158 0.994134 0.000000
    outer loop
      vertex 4.635033 66.101761 11.000000
      vertex 4.505862 66.115814 11.000000
      vertex 4.505862 66.115814 13.000000
    endloop
  endfacet
  facet normal 0.108158 0.994134 -0.000000
    outer loop
      vertex 4.635033 66.101761 11.000000
      vertex 4.505862 66.115814 13.000000
      vertex 4.635033 66.101761 13.000000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 4.764966 66.101761 11.000000
      vertex 4.635033 66.101761 11.000000
      vertex 4.635033 66.101761 13.000000
    endloop
  endfacet
  facet normal 0.000000 1.000000 -0.000000
    outer loop
      vertex 4.764966 66.101761 11.000000
      vertex 4.635033 66.101761 13.000000
      vertex 4.764966 66.101761 13.000000
    endloop
  endfacet
  facet normal -0.108158 0.994134 0.000000
    outer loop
      vertex 4.894138 66.115814 11.000000
      vertex 4.764966 66.101761 11.000000
      vertex 4.764966 66.101761 13.000000
    endloop
  endfacet
  facet normal -0.108158 0.994134 0.000000
    outer loop
      vertex 4.894138 66.115814 11.000000
      vertex 4.764966 66.101761 13.000000
      vertex 4.894138 66.115814 13.000000
    endloop
  endfacet
  facet normal -0.214966 0.976621 0.000000
    outer loop
      vertex 5.021034 66.143745 11.000000
      vertex 4.894138 66.115814 11.000000
      vertex 4.894138 66.115814 13.000000
    endloop
  endfacet
  facet normal -0.214966 0.976621 0.000000
    outer loop
      vertex 5.021034 66.143745 11.000000
      vertex 4.894138 66.115814 13.000000
      vertex 5.021034 66.143745 13.000000
    endloop
  endfacet
  facet normal -0.319253 0.947670 0.000000
    outer loop
      vertex 5.144166 66.185226 11.000000
      vertex 5.021034 66.143745 11.000000
      vertex 5.021034 66.143745 13.000000
    endloop
  endfacet
  facet normal -0.319253 0.947670 0.000000
    outer loop
      vertex 5.144166 66.185226 11.000000
      vertex 5.021034 66.143745 13.000000
      vertex 5.144166 66.185226 13.000000
    endloop
  endfacet
  facet normal -0.419939 0.907552 0.000000
    outer loop
      vertex 5.262090 66.239792 11.000000
      vertex 5.144166 66.185226 11.000000
      vertex 5.144166 66.185226 13.000000
    endloop
  endfacet
  facet normal -0.419939 0.907552 0.000000
    outer loop
      vertex 5.262090 66.239792 11.000000
      vertex 5.144166 66.185226 13.000000
      vertex 5.262090 66.239792 13.000000
    endloop
  endfacet
  facet normal -0.515502 0.856888 0.000000
    outer loop
      vertex 5.373425 66.306770 11.000000
      vertex 5.262090 66.239792 11.000000
      vertex 5.262090 66.239792 13.000000
    endloop
  endfacet
  facet normal -0.515502 0.856888 0.000000
    outer loop
      vertex 5.373425 66.306770 11.000000
      vertex 5.262090 66.239792 13.000000
      vertex 5.373425 66.306770 13.000000
    endloop
  endfacet
  facet normal -0.605194 0.796078 0.000000
    outer loop
      vertex 5.476863 66.385406 11.000000
      vertex 5.373425 66.306770 11.000000
      vertex 5.373425 66.306770 13.000000
    endloop
  endfacet
  facet normal -0.605194 0.796078 0.000000
    outer loop
      vertex 5.476863 66.385406 11.000000
      vertex 5.373425 66.306770 13.000000
      vertex 5.476863 66.385406 13.000000
    endloop
  endfacet
  facet normal -0.687669 0.726024 0.000000
    outer loop
      vertex 5.571195 66.474754 11.000000
      vertex 5.476863 66.385406 11.000000
      vertex 5.476863 66.385406 13.000000
    endloop
  endfacet
  facet normal -0.687669 0.726024 0.000000
    outer loop
      vertex 5.571195 66.474754 11.000000
      vertex 5.476863 66.385406 13.000000
      vertex 5.571195 66.474754 13.000000
    endloop
  endfacet
  facet normal -0.762185 0.647359 0.000000
    outer loop
      vertex 5.655312 66.573792 11.000000
      vertex 5.571195 66.474754 11.000000
      vertex 5.571195 66.474754 13.000000
    endloop
  endfacet
  facet normal -0.762185 0.647359 0.000000
    outer loop
      vertex 5.655312 66.573792 11.000000
      vertex 5.571195 66.474754 13.000000
      vertex 5.655312 66.573792 13.000000
    endloop
  endfacet
  facet normal -0.827688 0.561189 0.000000
    outer loop
      vertex 5.728229 66.681335 11.000000
      vertex 5.655312 66.573792 11.000000
      vertex 5.655312 66.573792 13.000000
    endloop
  endfacet
  facet normal -0.827688 0.561189 0.000000
    outer loop
      vertex 5.728229 66.681335 11.000000
      vertex 5.655312 66.573792 13.000000
      vertex 5.728229 66.681335 13.000000
    endloop
  endfacet
  facet normal -0.883515 0.468404 0.000000
    outer loop
      vertex 5.789091 66.796135 11.000000
      vertex 5.728229 66.681335 11.000000
      vertex 5.728229 66.681335 13.000000
    endloop
  endfacet
  facet normal -0.883515 0.468404 0.000000
    outer loop
      vertex 5.789091 66.796135 11.000000
      vertex 5.728229 66.681335 13.000000
      vertex 5.789091 66.796135 13.000000
    endloop
  endfacet
  facet normal -0.928976 0.370139 0.000000
    outer loop
      vertex 5.837184 66.916840 11.000000
      vertex 5.789091 66.796135 11.000000
      vertex 5.789091 66.796135 13.000000
    endloop
  endfacet
  facet normal -0.928976 0.370139 0.000000
    outer loop
      vertex 5.837184 66.916840 11.000000
      vertex 5.789091 66.796135 13.000000
      vertex 5.837184 66.916840 13.000000
    endloop
  endfacet
  facet normal -0.963551 0.267523 0.000000
    outer loop
      vertex 5.871944 67.042038 11.000000
      vertex 5.837184 66.916840 11.000000
      vertex 5.837184 66.916840 13.000000
    endloop
  endfacet
  facet normal -0.963551 0.267523 0.000000
    outer loop
      vertex 5.871944 67.042038 11.000000
      vertex 5.837184 66.916840 13.000000
      vertex 5.871944 67.042038 13.000000
    endloop
  endfacet
  facet normal -0.986826 0.161785 0.000000
    outer loop
      vertex 5.892965 67.170258 11.000000
      vertex 5.871944 67.042038 11.000000
      vertex 5.871944 67.042038 13.000000
    endloop
  endfacet
  facet normal -0.986826 0.161785 0.000000
    outer loop
      vertex 5.892965 67.170258 11.000000
      vertex 5.871944 67.042038 13.000000
      vertex 5.892965 67.170258 13.000000
    endloop
  endfacet
  facet normal -0.998533 0.054140 0.000000
    outer loop
      vertex 5.900000 67.300003 11.000000
      vertex 5.892965 67.170258 11.000000
      vertex 5.892965 67.170258 13.000000
    endloop
  endfacet
  facet normal -0.998533 0.054140 0.000000
    outer loop
      vertex 5.900000 67.300003 11.000000
      vertex 5.892965 67.170258 13.000000
      vertex 5.900000 67.300003 13.000000
    endloop
  endfacet
  facet normal 1.000000 0.000000 0.000000
    outer loop
      vertex 2.000000 2.000000 0.000000
      vertex 2.000000 39.500000 0.000000
      vertex 2.000000 39.500000 2.000000
    endloop
  endfacet
  facet normal 1.000000 0.000000 0.000000
    outer loop
      vertex 2.000000 2.000000 0.000000
      vertex 2.000000 39.500000 2.000000
      vertex 2.000000 2.000000 2.000000
    endloop
  endfacet
  facet normal -1.000000 0.000000 0.000000
    outer loop
      vertex 31.000000 0.000000 2.000000
      vertex 31.000000 0.000000 23.000000
      vertex 31.000000 71.000000 23.000000
    endloop
  endfacet
  facet normal -1.000000 0.000000 0.000000
    outer loop
      vertex 31.000000 0.000000 2.000000
      vertex 31.000000 71.000000 23.000000
      vertex 31.000000 71.000000 2.000000
    endloop
  endfacet
  facet normal 1.000000 0.000000 0.000000
    outer loop
      vertex 9.900000 0.000000 15.500000
      vertex 9.900000 -1.000000 15.500000
      vertex 9.900000 -1.000000 12.500000
    endloop
  endfacet
  facet normal 1.000000 0.000000 0.000000
    outer loop
      vertex 9.900000 0.000000 15.500000
      vertex 9.900000 -1.000000 12.500000
      vertex 9.900000 -0.000000 12.500000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 0.000000
    outer loop
      vertex -0.000000 62.299999 0.000000
      vertex 2.000000 62.299999 0.000000
      vertex 2.000000 62.299999 2.000000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 0.000000
    outer loop
      vertex -0.000000 62.299999 0.000000
      vertex 2.000000 62.299999 2.000000
      vertex 0.000000 62.299999 2.000000
    endloop
  endfacet
  facet normal -0.891008 -0.453988 -0.000000
    outer loop
      vertex 22.336454 -2.406737 -4.413546
      vertex 22.336454 -2.406737 -6.086455
      vertex 22.383974 -2.500000 -6.133975
    endloop
  endfacet
  facet normal -0.777147 -0.629320 -0.000000
    outer loop
      vertex 22.440983 -2.587785 -4.309017
      vertex 22.440983 -2.587785 -6.190983
      vertex 22.506855 -2.669131 -6.256855
    endloop
  endfacet
  facet normal -0.258822 -0.965925 -0.000000
    outer loop
      vertex 22.940983 -2.951056 -3.809017
      vertex 22.940983 -2.951056 -6.690983
      vertex 23.042088 -2.978148 -6.792089
    endloop
  endfacet
  facet normal -0.052334 -0.998630 -0.000000
    outer loop
      vertex 23.145472 -2.994522 -3.604528
      vertex 23.145472 -2.994522 -6.895472
      vertex 23.250000 -3.000000 -7.000000
    endloop
  endfacet
  facet normal -0.052334 -0.998630 0.000000
    outer loop
      vertex 23.145472 -2.994522 -3.604528
      vertex 23.250000 -3.000000 -7.000000
      vertex 23.250000 -3.000000 -3.500000
    endloop
  endfacet
  facet normal -0.156434 -0.987688 0.000000
    outer loop
      vertex 23.042088 -2.978148 -6.792089
      vertex 23.145472 -2.994522 -6.895472
      vertex 23.145472 -2.994522 -3.604528
    endloop
  endfacet
  facet normal -0.156434 -0.987688 0.000000
    outer loop
      vertex 23.042088 -2.978148 -6.792089
      vertex 23.145472 -2.994522 -3.604528
      vertex 23.042088 -2.978148 -3.707911
    endloop
  endfacet
  facet normal -0.258822 -0.965925 0.000000
    outer loop
      vertex 22.940983 -2.951056 -3.809017
      vertex 23.042088 -2.978148 -6.792089
      vertex 23.042088 -2.978148 -3.707911
    endloop
  endfacet
  facet normal -0.358370 -0.933580 0.000000
    outer loop
      vertex 22.843264 -2.913545 -6.593263
      vertex 22.940983 -2.951056 -6.690983
      vertex 22.940983 -2.951056 -3.809017
    endloop
  endfacet
  facet normal -0.358370 -0.933580 0.000000
    outer loop
      vertex 22.843264 -2.913545 -6.593263
      vertex 22.940983 -2.951056 -3.809017
      vertex 22.843264 -2.913545 -3.906737
    endloop
  endfacet
  facet normal -0.453990 -0.891007 0.000000
    outer loop
      vertex 22.750000 -2.866025 -6.500000
      vertex 22.843264 -2.913545 -6.593263
      vertex 22.843264 -2.913545 -3.906737
    endloop
  endfacet
  facet normal -0.453990 -0.891007 0.000000
    outer loop
      vertex 22.750000 -2.866025 -6.500000
      vertex 22.843264 -2.913545 -3.906737
      vertex 22.750000 -2.866025 -4.000000
    endloop
  endfacet
  facet normal -0.544636 -0.838673 0.000000
    outer loop
      vertex 22.662214 -2.809017 -6.412215
      vertex 22.750000 -2.866025 -6.500000
      vertex 22.750000 -2.866025 -4.000000
    endloop
  endfacet
  facet normal -0.544636 -0.838673 0.000000
    outer loop
      vertex 22.662214 -2.809017 -6.412215
      vertex 22.750000 -2.866025 -4.000000
      vertex 22.662214 -2.809017 -4.087785
    endloop
  endfacet
  facet normal -0.629324 -0.777143 0.000000
    outer loop
      vertex 22.580870 -2.743145 -6.330870
      vertex 22.662214 -2.809017 -6.412215
      vertex 22.662214 -2.809017 -4.087785
    endloop
  endfacet
  facet normal -0.629324 -0.777143 0.000000
    outer loop
      vertex 22.580870 -2.743145 -6.330870
      vertex 22.662214 -2.809017 -4.087785
      vertex 22.580870 -2.743145 -4.169131
    endloop
  endfacet
  facet normal -0.707103 -0.707110 0.000000
    outer loop
      vertex 22.506855 -2.669131 -6.256855
      vertex 22.580870 -2.743145 -6.330870
      vertex 22.580870 -2.743145 -4.169131
    endloop
  endfacet
  facet normal -0.707103 -0.707110 0.000000
    outer loop
      vertex 22.506855 -2.669131 -6.256855
      vertex 22.580870 -2.743145 -4.169131
      vertex 22.506855 -2.669131 -4.243145
    endloop
  endfacet
  facet normal -0.777147 -0.629320 0.000000
    outer loop
      vertex 22.440983 -2.587785 -4.309017
      vertex 22.506855 -2.669131 -6.256855
      vertex 22.506855 -2.669131 -4.243145
    endloop
  endfacet
  facet normal -0.838669 -0.544641 0.000000
    outer loop
      vertex 22.383974 -2.500000 -6.133975
      vertex 22.440983 -2.587785 -6.190983
      vertex 22.440983 -2.587785 -4.309017
    endloop
  endfacet
  facet normal -0.838669 -0.544641 0.000000
    outer loop
      vertex 22.383974 -2.500000 -6.133975
      vertex 22.440983 -2.587785 -4.309017
      vertex 22.383974 -2.500000 -4.366025
    endloop
  endfacet
  facet normal -0.891008 -0.453988 0.000000
    outer loop
      vertex 22.336454 -2.406737 -4.413546
      vertex 22.383974 -2.500000 -6.133975
      vertex 22.383974 -2.500000 -4.366025
    endloop
  endfacet
  facet normal -0.933578 -0.358374 0.000000
    outer loop
      vertex 22.298943 -2.309017 -6.048944
      vertex 22.336454 -2.406737 -6.086455
      vertex 22.336454 -2.406737 -4.413546
    endloop
  endfacet
  facet normal -0.933578 -0.358374 0.000000
    outer loop
      vertex 22.298943 -2.309017 -6.048944
      vertex 22.336454 -2.406737 -4.413546
      vertex 22.298943 -2.309017 -4.451056
    endloop
  endfacet
  facet normal -0.965928 -0.258810 0.000000
    outer loop
      vertex 22.271852 -2.207912 -6.021852
      vertex 22.298943 -2.309017 -6.048944
      vertex 22.298943 -2.309017 -4.451056
    endloop
  endfacet
  facet normal -0.965928 -0.258810 0.000000
    outer loop
      vertex 22.271852 -2.207912 -6.021852
      vertex 22.298943 -2.309017 -4.451056
      vertex 22.271852 -2.207912 -4.478148
    endloop
  endfacet
  facet normal -0.987688 -0.156437 0.000000
    outer loop
      vertex 22.255478 -2.104528 -6.005478
      vertex 22.271852 -2.207912 -6.021852
      vertex 22.271852 -2.207912 -4.478148
    endloop
  endfacet
  facet normal -0.987688 -0.156437 0.000000
    outer loop
      vertex 22.255478 -2.104528 -6.005478
      vertex 22.271852 -2.207912 -4.478148
      vertex 22.255478 -2.104528 -4.494522
    endloop
  endfacet
  facet normal -0.998630 -0.052334 0.000000
    outer loop
      vertex 22.255478 -2.104528 -6.005478
      vertex 22.255478 -2.104528 -4.494522
      vertex 22.250000 -2.000000 -4.500000
    endloop
  endfacet
  facet normal -0.998630 -0.052334 0.000000
    outer loop
      vertex 22.250000 -2.000000 -6.000000
      vertex 22.255478 -2.104528 -6.005478
      vertex 22.250000 -2.000000 -4.500000
    endloop
  endfacet
  facet normal -0.284011 0.000000 0.958821
    outer loop
      vertex -1.888229 7.948888 15.948888
      vertex -1.888229 14.051111 15.948888
      vertex -1.963526 14.073416 15.926584
    endloop
  endfacet
  facet normal -0.477150 0.000000 0.878822
    outer loop
      vertex -2.180986 7.836510 15.836509
      vertex -2.180986 14.163490 15.836509
      vertex -2.250000 14.200962 15.799038
    endloop
  endfacet
  facet normal -0.998629 0.000000 0.052337
    outer loop
      vertex -2.991783 6.656793 14.656793
      vertex -3.000000 15.500000 14.500000
      vertex -3.000000 6.500000 14.500000
    endloop
  endfacet
  facet normal -0.998629 0.000000 0.052337
    outer loop
      vertex -2.991783 15.343207 14.656793
      vertex -3.000000 15.500000 14.500000
      vertex -2.991783 6.656793 14.656793
    endloop
  endfacet
  facet normal -0.987689 0.000000 0.156433
    outer loop
      vertex -2.991783 15.343207 14.656793
      vertex -2.991783 6.656793 14.656793
      vertex -2.967221 6.811867 14.811868
    endloop
  endfacet
  facet normal -0.987689 0.000000 0.156433
    outer loop
      vertex -2.967221 15.188132 14.811868
      vertex -2.991783 15.343207 14.656793
      vertex -2.967221 6.811867 14.811868
    endloop
  endfacet
  facet normal -0.965926 0.000000 0.258820
    outer loop
      vertex -2.967221 15.188132 14.811868
      vertex -2.967221 6.811867 14.811868
      vertex -2.926585 6.963525 14.963526
    endloop
  endfacet
  facet normal -0.965926 0.000000 0.258820
    outer loop
      vertex -2.926585 15.036475 14.963526
      vertex -2.967221 15.188132 14.811868
      vertex -2.926585 6.963525 14.963526
    endloop
  endfacet
  facet normal -0.933581 0.000000 0.358367
    outer loop
      vertex -2.926585 15.036475 14.963526
      vertex -2.926585 6.963525 14.963526
      vertex -2.870318 7.110105 15.110106
    endloop
  endfacet
  facet normal -0.933581 0.000000 0.358367
    outer loop
      vertex -2.870318 14.889895 15.110106
      vertex -2.926585 15.036475 14.963526
      vertex -2.870318 7.110105 15.110106
    endloop
  endfacet
  facet normal -0.891006 0.000000 0.453992
    outer loop
      vertex -2.870318 14.889895 15.110106
      vertex -2.870318 7.110105 15.110106
      vertex -2.799038 7.250000 15.250000
    endloop
  endfacet
  facet normal -0.891006 0.000000 0.453992
    outer loop
      vertex -2.799038 14.750000 15.250000
      vertex -2.870318 14.889895 15.110106
      vertex -2.799038 7.250000 15.250000
    endloop
  endfacet
  facet normal -0.838670 0.000000 0.544640
    outer loop
      vertex -2.799038 14.750000 15.250000
      vertex -2.799038 7.250000 15.250000
      vertex -2.713526 7.381678 15.381678
    endloop
  endfacet
  facet normal -0.838670 0.000000 0.544640
    outer loop
      vertex -2.713526 14.618322 15.381678
      vertex -2.799038 14.750000 15.250000
      vertex -2.713526 7.381678 15.381678
    endloop
  endfacet
  facet normal -0.777148 0.000000 0.629318
    outer loop
      vertex -2.713526 14.618322 15.381678
      vertex -2.713526 7.381678 15.381678
      vertex -2.614717 7.503696 15.503696
    endloop
  endfacet
  facet normal -0.777148 0.000000 0.629318
    outer loop
      vertex -2.614717 14.496305 15.503696
      vertex -2.713526 14.618322 15.381678
      vertex -2.614717 7.503696 15.503696
    endloop
  endfacet
  facet normal -0.707106 0.000000 0.707108
    outer loop
      vertex -2.614717 14.496305 15.503696
      vertex -2.614717 7.503696 15.503696
      vertex -2.503696 7.614717 15.614717
    endloop
  endfacet
  facet normal -0.707106 0.000000 0.707108
    outer loop
      vertex -2.503696 14.385283 15.614717
      vertex -2.614717 14.496305 15.503696
      vertex -2.503696 7.614717 15.614717
    endloop
  endfacet
  facet normal -0.629320 0.000000 0.777146
    outer loop
      vertex -2.503696 14.385283 15.614717
      vertex -2.503696 7.614717 15.614717
      vertex -2.381678 7.713526 15.713526
    endloop
  endfacet
  facet normal -0.629320 0.000000 0.777146
    outer loop
      vertex -2.381678 14.286474 15.713526
      vertex -2.503696 14.385283 15.614717
      vertex -2.381678 7.713526 15.713526
    endloop
  endfacet
  facet normal -0.566405 0.000000 0.824127
    outer loop
      vertex -2.381678 14.286474 15.713526
      vertex -2.381678 7.713526 15.713526
      vertex -2.316958 7.758006 15.758006
    endloop
  endfacet
  facet normal -0.566405 0.000000 0.824127
    outer loop
      vertex -2.316958 14.241994 15.758006
      vertex -2.381678 14.286474 15.713526
      vertex -2.316958 7.758006 15.758006
    endloop
  endfacet
  facet normal -0.522495 0.000000 0.852642
    outer loop
      vertex -2.250000 14.200962 15.799038
      vertex -2.316958 14.241994 15.758006
      vertex -2.316958 7.758006 15.758006
    endloop
  endfacet
  facet normal -0.522495 0.000000 0.852642
    outer loop
      vertex -2.250000 14.200962 15.799038
      vertex -2.316958 7.758006 15.758006
      vertex -2.250000 7.799038 15.799038
    endloop
  endfacet
  facet normal -0.477150 0.000000 0.878822
    outer loop
      vertex -2.180986 7.836510 15.836509
      vertex -2.250000 14.200962 15.799038
      vertex -2.250000 7.799038 15.799038
    endloop
  endfacet
  facet normal -0.430515 0.000000 0.902583
    outer loop
      vertex -2.110105 14.129682 15.870317
      vertex -2.180986 14.163490 15.836509
      vertex -2.180986 7.836510 15.836509
    endloop
  endfacet
  facet normal -0.430515 0.000000 0.902583
    outer loop
      vertex -2.110105 14.129682 15.870317
      vertex -2.180986 7.836510 15.836509
      vertex -2.110105 7.870318 15.870317
    endloop
  endfacet
  facet normal -0.382680 0.000000 0.923881
    outer loop
      vertex -2.037552 14.099629 15.900370
      vertex -2.110105 14.129682 15.870317
      vertex -2.110105 7.870318 15.870317
    endloop
  endfacet
  facet normal -0.382680 0.000000 0.923881
    outer loop
      vertex -2.037552 14.099629 15.900370
      vertex -2.110105 7.870318 15.870317
      vertex -2.037552 7.900370 15.900370
    endloop
  endfacet
  facet normal -0.333812 0.000000 0.942639
    outer loop
      vertex -1.963526 14.073416 15.926584
      vertex -2.037552 14.099629 15.900370
      vertex -2.037552 7.900370 15.900370
    endloop
  endfacet
  facet normal -0.333812 0.000000 0.942640
    outer loop
      vertex -1.963526 14.073416 15.926584
      vertex -2.037552 7.900370 15.900370
      vertex -1.963526 7.926585 15.926584
    endloop
  endfacet
  facet normal -0.284011 0.000000 0.958821
    outer loop
      vertex -1.888229 7.948888 15.948888
      vertex -1.963526 14.073416 15.926584
      vertex -1.963526 7.926585 15.926584
    endloop
  endfacet
  facet normal -0.233466 0.000000 0.972365
    outer loop
      vertex -1.811868 14.032779 15.967222
      vertex -1.888229 14.051111 15.948888
      vertex -1.888229 7.948888 15.948888
    endloop
  endfacet
  facet normal -0.233466 0.000000 0.972365
    outer loop
      vertex -1.811868 14.032779 15.967222
      vertex -1.888229 7.948888 15.948888
      vertex -1.811868 7.967222 15.967222
    endloop
  endfacet
  facet normal -0.182232 0.000000 0.983256
    outer loop
      vertex -1.734652 14.018468 15.981533
      vertex -1.811868 14.032779 15.967222
      vertex -1.811868 7.967222 15.967222
    endloop
  endfacet
  facet normal -0.182232 0.000000 0.983256
    outer loop
      vertex -1.734652 14.018468 15.981533
      vertex -1.811868 7.967222 15.967222
      vertex -1.734652 7.981532 15.981533
    endloop
  endfacet
  facet normal -0.130523 0.000000 0.991445
    outer loop
      vertex -1.656793 14.008218 15.991783
      vertex -1.734652 14.018468 15.981533
      vertex -1.734652 7.981532 15.981533
    endloop
  endfacet
  facet normal -0.026170 0.000000 0.999658
    outer loop
      vertex -1.500000 14.000000 16.000000
      vertex -1.578504 7.997944 15.997945
      vertex -1.500000 8.000000 16.000000
    endloop
  endfacet
  facet normal -0.130523 0.000000 0.991445
    outer loop
      vertex -1.656793 14.008218 15.991783
      vertex -1.734652 7.981532 15.981533
      vertex -1.656793 7.991782 15.991783
    endloop
  endfacet
  facet normal -0.078462 0.000000 0.996917
    outer loop
      vertex -1.656793 14.008218 15.991783
      vertex -1.656793 7.991782 15.991783
      vertex -1.578504 7.997944 15.997945
    endloop
  endfacet
  facet normal -0.078462 0.000000 0.996917
    outer loop
      vertex -1.578504 14.002056 15.997945
      vertex -1.656793 14.008218 15.991783
      vertex -1.578504 7.997944 15.997945
    endloop
  endfacet
  facet normal -0.026170 0.000000 0.999658
    outer loop
      vertex -1.578504 14.002056 15.997945
      vertex -1.578504 7.997944 15.997945
      vertex -1.500000 14.000000 16.000000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 0.000000
    outer loop
      vertex 2.000000 69.000000 0.000000
      vertex 29.000000 69.000000 0.000000
      vertex 29.000000 69.000000 2.000000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 0.000000
    outer loop
      vertex 2.000000 69.000000 0.000000
      vertex 29.000000 69.000000 2.000000
      vertex 2.000000 69.000000 2.000000
    endloop
  endfacet
  facet normal 1.000000 0.000000 0.000000
    outer loop
      vertex 7.750000 -1.000000 -6.500000
      vertex 7.750000 3.000000 -6.500000
      vertex 7.750000 3.000000 -4.500000
    endloop
  endfacet
  facet normal 1.000000 0.000000 0.000000
    outer loop
      vertex 7.750000 -1.000000 -6.500000
      vertex 7.750000 3.000000 -4.500000
      vertex 7.750000 -1.000000 -4.500000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 22.000000 0.000000 15.500000
      vertex 22.000000 0.000000 23.000000
      vertex 31.000000 0.000000 23.000000
    endloop
  endfacet
  facet normal -0.000000 1.000000 0.000000
    outer loop
      vertex 22.000000 0.000000 15.500000
      vertex 31.000000 0.000000 23.000000
      vertex 31.000000 0.000000 2.000000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 0.000000 0.000000 2.000000
      vertex 0.000000 0.000000 23.000000
      vertex 7.000000 0.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 0.000000 0.000000 2.000000
      vertex 7.000000 0.000000 23.000000
      vertex 7.000000 0.000000 15.500000
    endloop
  endfacet
  facet normal 0.000000 1.000000 -0.000000
    outer loop
      vertex 18.400000 -0.000000 12.500000
      vertex 18.400000 0.000000 15.500000
      vertex 22.000000 0.000000 15.500000
    endloop
  endfacet
  facet normal -0.000000 1.000000 -0.000000
    outer loop
      vertex 18.400000 -0.000000 12.500000
      vertex 22.000000 0.000000 15.500000
      vertex 31.000000 0.000000 2.000000
    endloop
  endfacet
  facet normal -0.000000 1.000000 0.000000
    outer loop
      vertex 9.900000 -0.000000 12.500000
      vertex 18.400000 -0.000000 12.500000
      vertex 31.000000 0.000000 2.000000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 9.900000 -0.000000 12.500000
      vertex 31.000000 0.000000 2.000000
      vertex 0.000000 0.000000 2.000000
    endloop
  endfacet
  facet normal 0.000000 1.000000 -0.000000
    outer loop
      vertex 9.900000 0.000000 15.500000
      vertex 9.900000 -0.000000 12.500000
      vertex 0.000000 0.000000 2.000000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 9.900000 0.000000 15.500000
      vertex 0.000000 0.000000 2.000000
      vertex 7.000000 0.000000 15.500000
    endloop
  endfacet
  facet normal -1.000000 0.000000 0.000000
    outer loop
      vertex 22.250000 -2.000000 -6.000000
      vertex 22.250000 -2.000000 -4.500000
      vertex 22.250000 -1.000000 -4.500000
    endloop
  endfacet
  facet normal -1.000000 0.000000 0.000000
    outer loop
      vertex 22.250000 -2.000000 -6.000000
      vertex 22.250000 -1.000000 -4.500000
      vertex 22.250000 -1.000000 -6.000000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 2.000000 2.000000 0.000000
      vertex 2.000000 2.000000 2.000000
      vertex 29.000000 2.000000 2.000000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 2.000000 2.000000 0.000000
      vertex 29.000000 2.000000 2.000000
      vertex 29.000000 2.000000 0.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.500000 14.000000 16.000000
      vertex -1.500000 8.000000 16.000000
      vertex 0.000000 8.000000 16.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex -1.500000 14.000000 16.000000
      vertex 0.000000 8.000000 16.000000
      vertex 0.000000 14.000000 16.000000
    endloop
  endfacet
  facet normal 1.000000 0.000000 -0.000000
    outer loop
      vertex 2.000000 69.000000 0.000000
      vertex 2.000000 69.000000 2.000000
      vertex 2.000000 62.299999 2.000000
    endloop
  endfacet
  facet normal 1.000000 0.000000 0.000000
    outer loop
      vertex 2.000000 69.000000 0.000000
      vertex 2.000000 62.299999 2.000000
      vertex 2.000000 62.299999 0.000000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 0.000000
    outer loop
      vertex -1.500000 14.000000 20.500000
      vertex -1.500000 14.000000 16.000000
      vertex 0.000000 14.000000 16.000000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 0.000000
    outer loop
      vertex -1.500000 14.000000 20.500000
      vertex 0.000000 14.000000 16.000000
      vertex 0.000000 14.000000 20.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 34.000000 71.099998 23.000000
      vertex 32.758125 71.744560 23.000000
      vertex 32.685486 71.587555 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 34.000000 71.099998 23.000000
      vertex 32.685486 71.587555 23.000000
      vertex 32.580795 71.449837 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 34.000000 71.099998 23.000000
      vertex 32.580795 71.449837 23.000000
      vertex 32.448952 71.337852 23.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 32.296108 71.256813 23.000000
      vertex 34.000000 71.099998 23.000000
      vertex 32.448952 71.337852 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.100000 74.000000 23.000000
      vertex 31.363127 71.515862 23.000000
      vertex 31.273939 71.664085 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 74.000000 23.000000
      vertex 31.551052 72.662155 23.000000
      vertex 31.703890 72.743187 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 74.000000 23.000000
      vertex 31.703890 72.743187 23.000000
      vertex 31.870573 72.789459 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.209057 73.989044 23.000000
      vertex 32.000000 74.000000 23.000000
      vertex 31.870573 72.789459 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.209057 73.989044 23.000000
      vertex 31.870573 72.789459 23.000000
      vertex 32.043312 72.798828 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.415821 73.956299 23.000000
      vertex 32.209057 73.989044 23.000000
      vertex 32.043312 72.798828 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.415821 73.956299 23.000000
      vertex 32.043312 72.798828 23.000000
      vertex 32.214024 72.770844 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.795311 71.913506 23.000000
      vertex 32.758125 71.744560 23.000000
      vertex 34.000000 71.099998 23.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 32.795311 71.913506 23.000000
      vertex 34.000000 71.099998 23.000000
      vertex 34.000000 72.000000 23.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 32.799999 72.000000 23.000000
      vertex 32.795311 71.913506 23.000000
      vertex 34.000000 72.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.799999 72.000000 23.000000
      vertex 34.000000 72.000000 23.000000
      vertex 33.989040 72.209061 23.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 32.781296 72.171982 23.000000
      vertex 32.799999 72.000000 23.000000
      vertex 33.989040 72.209061 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.100000 74.000000 23.000000
      vertex 31.956688 71.201172 23.000000
      vertex 31.785976 71.229156 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.100000 74.000000 23.000000
      vertex 31.785976 71.229156 23.000000
      vertex 31.625275 71.293190 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.781296 72.171982 23.000000
      vertex 33.989040 72.209061 23.000000
      vertex 33.956295 72.415825 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.781296 72.171982 23.000000
      vertex 33.956295 72.415825 23.000000
      vertex 33.902111 72.618034 23.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 32.726059 72.335915 23.000000
      vertex 32.781296 72.171982 23.000000
      vertex 33.902111 72.618034 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.100000 74.000000 23.000000
      vertex 31.273939 71.664085 23.000000
      vertex 31.218704 71.828026 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.100000 74.000000 23.000000
      vertex 31.218704 71.828026 23.000000
      vertex 31.199999 72.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 31.218704 72.171982 23.000000
      vertex -0.100000 74.000000 23.000000
      vertex 31.199999 72.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.100000 74.000000 23.000000
      vertex 31.218704 72.171982 23.000000
      vertex 31.273939 72.335915 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.100000 74.000000 23.000000
      vertex 31.273939 72.335915 23.000000
      vertex 31.363127 72.484146 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 74.000000 23.000000
      vertex -0.100000 74.000000 23.000000
      vertex 31.363127 72.484146 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 74.000000 23.000000
      vertex 31.363127 72.484146 23.000000
      vertex 31.482090 72.609734 23.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 31.551052 72.662155 23.000000
      vertex 32.000000 74.000000 23.000000
      vertex 31.482090 72.609734 23.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 32.214024 72.770844 23.000000
      vertex 32.374729 72.706810 23.000000
      vertex 32.813473 73.827087 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.214024 72.770844 23.000000
      vertex 32.813473 73.827087 23.000000
      vertex 32.618034 73.902115 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.415821 73.956299 23.000000
      vertex 32.214024 72.770844 23.000000
      vertex 32.618034 73.902115 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.100000 74.000000 23.000000
      vertex 31.625275 71.293190 23.000000
      vertex 31.551052 71.337852 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.100000 74.000000 23.000000
      vertex 31.551052 71.337852 23.000000
      vertex 31.482090 71.390274 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 31.363127 71.515862 23.000000
      vertex -0.100000 74.000000 23.000000
      vertex 31.482090 71.390274 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.726059 72.335915 23.000000
      vertex 33.902111 72.618034 23.000000
      vertex 33.827091 72.813477 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.726059 72.335915 23.000000
      vertex 33.827091 72.813477 23.000000
      vertex 33.732048 73.000000 23.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 32.636875 72.484146 23.000000
      vertex 32.726059 72.335915 23.000000
      vertex 33.732048 73.000000 23.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 32.374729 72.706810 23.000000
      vertex 32.517910 72.609734 23.000000
      vertex 33.175568 73.618034 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.374729 72.706810 23.000000
      vertex 33.175568 73.618034 23.000000
      vertex 33.000000 73.732048 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.813473 73.827087 23.000000
      vertex 32.374729 72.706810 23.000000
      vertex 33.000000 73.732048 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.636875 72.484146 23.000000
      vertex 33.732048 73.000000 23.000000
      vertex 33.618034 73.175575 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.636875 72.484146 23.000000
      vertex 33.618034 73.175575 23.000000
      vertex 33.486286 73.338264 23.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 32.517910 72.609734 23.000000
      vertex 32.636875 72.484146 23.000000
      vertex 33.486286 73.338264 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.517910 72.609734 23.000000
      vertex 33.486286 73.338264 23.000000
      vertex 33.338261 73.486290 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 33.175568 73.618034 23.000000
      vertex 32.517910 72.609734 23.000000
      vertex 33.338261 73.486290 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 22.000000 -1.500000 23.000000
      vertex 7.000000 -1.500000 23.000000
      vertex -0.100000 -3.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 22.000000 -1.500000 23.000000
      vertex -0.100000 -3.000000 23.000000
      vertex 32.000000 -3.000000 23.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 32.685486 -1.412443 23.000000
      vertex 33.827091 -1.813473 23.000000
      vertex 32.758125 -1.255441 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.685486 -1.412443 23.000000
      vertex 32.580795 -1.550160 23.000000
      vertex 33.618034 -2.175570 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.685486 -1.412443 23.000000
      vertex 33.618034 -2.175570 23.000000
      vertex 33.732048 -2.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 33.827091 -1.813473 23.000000
      vertex 32.685486 -1.412443 23.000000
      vertex 33.732048 -2.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.580795 -1.550160 23.000000
      vertex 32.448952 -1.662151 23.000000
      vertex 33.338261 -2.486290 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.580795 -1.550160 23.000000
      vertex 33.338261 -2.486290 23.000000
      vertex 33.486286 -2.338261 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 33.618034 -2.175570 23.000000
      vertex 32.580795 -1.550160 23.000000
      vertex 33.486286 -2.338261 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.448952 -1.662151 23.000000
      vertex 32.296108 -1.743181 23.000000
      vertex 33.000000 -2.732051 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.448952 -1.662151 23.000000
      vertex 33.000000 -2.732051 23.000000
      vertex 33.175568 -2.618034 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 33.338261 -2.486290 23.000000
      vertex 32.448952 -1.662151 23.000000
      vertex 33.175568 -2.618034 23.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex -0.100000 71.099998 23.000000
      vertex 31.000000 71.000000 23.000000
      vertex 34.000000 71.099998 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 22.000000 -1.500000 23.000000
      vertex 31.363127 -1.484139 23.000000
      vertex 31.273939 -1.335911 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 22.000000 -1.500000 23.000000
      vertex 31.273939 -1.335911 23.000000
      vertex 31.218704 -1.171976 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.100000 -3.000000 23.000000
      vertex 7.000000 -1.500000 23.000000
      vertex 7.000000 0.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.100000 -3.000000 23.000000
      vertex 7.000000 0.000000 23.000000
      vertex 0.000000 0.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.100000 71.099998 23.000000
      vertex -0.100000 -3.000000 23.000000
      vertex 0.000000 0.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.100000 71.099998 23.000000
      vertex 0.000000 0.000000 23.000000
      vertex -0.000000 71.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 31.000000 71.000000 23.000000
      vertex -0.100000 71.099998 23.000000
      vertex -0.000000 71.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 31.218704 -1.171976 23.000000
      vertex 31.199999 -1.000000 23.000000
      vertex 31.000000 0.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 31.218704 -1.171976 23.000000
      vertex 31.000000 0.000000 23.000000
      vertex 22.000000 0.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 22.000000 -1.500000 23.000000
      vertex 31.218704 -1.171976 23.000000
      vertex 22.000000 0.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.296108 -1.743181 23.000000
      vertex 32.129425 -1.789461 23.000000
      vertex 32.618034 -2.902113 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.296108 -1.743181 23.000000
      vertex 32.618034 -2.902113 23.000000
      vertex 32.813473 -2.827091 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 33.000000 -2.732051 23.000000
      vertex 32.296108 -1.743181 23.000000
      vertex 32.813473 -2.827091 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 31.956688 -1.798827 23.000000
      vertex 31.785976 -1.770840 23.000000
      vertex 32.000000 -3.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 31.956688 -1.798827 23.000000
      vertex 32.000000 -3.000000 23.000000
      vertex 32.209057 -2.989044 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.129425 -1.789461 23.000000
      vertex 31.956688 -1.798827 23.000000
      vertex 32.209057 -2.989044 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.129425 -1.789461 23.000000
      vertex 32.209057 -2.989044 23.000000
      vertex 32.415821 -2.956295 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.618034 -2.902113 23.000000
      vertex 32.129425 -1.789461 23.000000
      vertex 32.415821 -2.956295 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 34.000000 -1.000000 23.000000
      vertex 32.636875 -0.515861 23.000000
      vertex 32.726059 -0.664089 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 -3.000000 23.000000
      vertex 31.785976 -1.770840 23.000000
      vertex 31.625275 -1.706810 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 -3.000000 23.000000
      vertex 31.625275 -1.706810 23.000000
      vertex 31.551052 -1.662151 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 22.000000 -1.500000 23.000000
      vertex 32.000000 -3.000000 23.000000
      vertex 31.551052 -1.662151 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 22.000000 -1.500000 23.000000
      vertex 31.551052 -1.662151 23.000000
      vertex 31.482090 -1.609730 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 31.363127 -1.484139 23.000000
      vertex 22.000000 -1.500000 23.000000
      vertex 31.482090 -1.609730 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.758125 -1.255441 23.000000
      vertex 33.827091 -1.813473 23.000000
      vertex 33.902111 -1.618034 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.758125 -1.255441 23.000000
      vertex 33.902111 -1.618034 23.000000
      vertex 33.956295 -1.415823 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.795311 -1.086495 23.000000
      vertex 32.758125 -1.255441 23.000000
      vertex 33.956295 -1.415823 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.795311 -1.086495 23.000000
      vertex 33.956295 -1.415823 23.000000
      vertex 33.989040 -1.209057 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.799999 -1.000000 23.000000
      vertex 32.795311 -1.086495 23.000000
      vertex 33.989040 -1.209057 23.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 32.799999 -1.000000 23.000000
      vertex 33.989040 -1.209057 23.000000
      vertex 34.000000 -1.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.781296 -0.828024 23.000000
      vertex 32.799999 -1.000000 23.000000
      vertex 34.000000 -1.000000 23.000000
    endloop
  endfacet
  facet normal -0.000000 -0.000000 1.000000
    outer loop
      vertex 32.781296 -0.828024 23.000000
      vertex 34.000000 -1.000000 23.000000
      vertex 32.726059 -0.664089 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 34.000000 71.099998 23.000000
      vertex 32.043312 -0.201173 23.000000
      vertex 32.214024 -0.229160 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 34.000000 71.099998 23.000000
      vertex 32.214024 -0.229160 23.000000
      vertex 32.374729 -0.293190 23.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 34.000000 -1.000000 23.000000
      vertex 34.000000 71.099998 23.000000
      vertex 32.374729 -0.293190 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 34.000000 -1.000000 23.000000
      vertex 32.374729 -0.293190 23.000000
      vertex 32.517910 -0.390270 23.000000
    endloop
  endfacet
  facet normal -0.000000 -0.000000 1.000000
    outer loop
      vertex 32.636875 -0.515861 23.000000
      vertex 34.000000 -1.000000 23.000000
      vertex 32.517910 -0.390270 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 31.000000 0.000000 23.000000
      vertex 31.199999 -1.000000 23.000000
      vertex 31.218704 -0.828024 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 31.000000 0.000000 23.000000
      vertex 31.218704 -0.828024 23.000000
      vertex 31.273939 -0.664089 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 31.363127 -0.515861 23.000000
      vertex 31.000000 0.000000 23.000000
      vertex 31.273939 -0.664089 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 31.000000 0.000000 23.000000
      vertex 31.363127 -0.515861 23.000000
      vertex 31.482090 -0.390270 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 31.000000 0.000000 23.000000
      vertex 31.482090 -0.390270 23.000000
      vertex 31.551052 -0.337849 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 31.000000 71.000000 23.000000
      vertex 31.000000 0.000000 23.000000
      vertex 31.551052 -0.337849 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 31.000000 71.000000 23.000000
      vertex 31.551052 -0.337849 23.000000
      vertex 31.703890 -0.256819 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 34.000000 71.099998 23.000000
      vertex 31.000000 71.000000 23.000000
      vertex 31.703890 -0.256819 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 34.000000 71.099998 23.000000
      vertex 31.703890 -0.256819 23.000000
      vertex 31.870573 -0.210539 23.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 32.043312 -0.201173 23.000000
      vertex 34.000000 71.099998 23.000000
      vertex 31.870573 -0.210539 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.100000 71.099998 23.000000
      vertex -0.363126 -0.515861 23.000000
      vertex -0.273940 -0.664089 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.200000 -1.000000 23.000000
      vertex -0.204690 -1.086495 23.000000
      vertex -0.100000 -3.000000 23.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex -0.200000 -1.000000 23.000000
      vertex -0.100000 -3.000000 23.000000
      vertex -0.100000 71.099998 23.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex -0.218704 -0.828024 23.000000
      vertex -0.200000 -1.000000 23.000000
      vertex -0.100000 71.099998 23.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex -0.218704 -0.828024 23.000000
      vertex -0.100000 71.099998 23.000000
      vertex -0.273940 -0.664089 23.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex -2.732051 -2.000000 23.000000
      vertex -1.726060 -1.335911 23.000000
      vertex -2.827091 -1.813473 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -3.000000 71.099998 23.000000
      vertex -3.000000 -1.000000 23.000000
      vertex -1.726060 -0.664089 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -3.000000 71.099998 23.000000
      vertex -1.726060 -0.664089 23.000000
      vertex -1.636874 -0.515861 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.517909 -0.390270 23.000000
      vertex -3.000000 71.099998 23.000000
      vertex -1.636874 -0.515861 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.100000 71.099998 23.000000
      vertex -0.956689 -0.201173 23.000000
      vertex -0.785977 -0.229160 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.100000 -3.000000 23.000000
      vertex -0.204690 -1.086495 23.000000
      vertex -0.241877 -1.255441 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.100000 -3.000000 23.000000
      vertex -0.241877 -1.255441 23.000000
      vertex -0.314514 -1.412443 23.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex -0.419204 -1.550160 23.000000
      vertex -0.100000 -3.000000 23.000000
      vertex -0.314514 -1.412443 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.636874 -1.484139 23.000000
      vertex -1.726060 -1.335911 23.000000
      vertex -2.732051 -2.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.100000 71.099998 23.000000
      vertex -0.785977 -0.229160 23.000000
      vertex -0.625273 -0.293190 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.100000 71.099998 23.000000
      vertex -0.625273 -0.293190 23.000000
      vertex -0.482091 -0.390270 23.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex -0.363126 -0.515861 23.000000
      vertex -0.100000 71.099998 23.000000
      vertex -0.482091 -0.390270 23.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex -2.902113 -1.618034 23.000000
      vertex -2.827091 -1.813473 23.000000
      vertex -1.726060 -1.335911 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -2.902113 -1.618034 23.000000
      vertex -1.726060 -1.335911 23.000000
      vertex -1.781296 -1.171976 23.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex -2.956295 -1.415823 23.000000
      vertex -2.902113 -1.618034 23.000000
      vertex -1.781296 -1.171976 23.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex -2.989044 -1.209057 23.000000
      vertex -2.956295 -1.415823 23.000000
      vertex -1.781296 -1.171976 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -2.989044 -1.209057 23.000000
      vertex -1.781296 -1.171976 23.000000
      vertex -1.800000 -1.000000 23.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex -3.000000 -1.000000 23.000000
      vertex -2.989044 -1.209057 23.000000
      vertex -1.800000 -1.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -3.000000 -1.000000 23.000000
      vertex -1.800000 -1.000000 23.000000
      vertex -1.781296 -0.828024 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.726060 -0.664089 23.000000
      vertex -3.000000 -1.000000 23.000000
      vertex -1.781296 -0.828024 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -3.000000 71.099998 23.000000
      vertex -1.517909 -0.390270 23.000000
      vertex -1.448950 -0.337849 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -3.000000 71.099998 23.000000
      vertex -1.448950 -0.337849 23.000000
      vertex -1.296111 -0.256819 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.100000 71.099998 23.000000
      vertex -3.000000 71.099998 23.000000
      vertex -1.296111 -0.256819 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.100000 71.099998 23.000000
      vertex -1.296111 -0.256819 23.000000
      vertex -1.129426 -0.210539 23.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex -0.956689 -0.201173 23.000000
      vertex -0.100000 71.099998 23.000000
      vertex -1.129426 -0.210539 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.374727 -1.706810 23.000000
      vertex -1.448950 -1.662151 23.000000
      vertex -2.000000 -2.732051 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.374727 -1.706810 23.000000
      vertex -2.000000 -2.732051 23.000000
      vertex -1.813473 -2.827091 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.214023 -1.770840 23.000000
      vertex -1.374727 -1.706810 23.000000
      vertex -1.813473 -2.827091 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.636874 -1.484139 23.000000
      vertex -2.732051 -2.000000 23.000000
      vertex -2.618034 -2.175570 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.636874 -1.484139 23.000000
      vertex -2.618034 -2.175570 23.000000
      vertex -2.486290 -2.338261 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.517909 -1.609730 23.000000
      vertex -1.636874 -1.484139 23.000000
      vertex -2.486290 -2.338261 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.517909 -1.609730 23.000000
      vertex -2.486290 -2.338261 23.000000
      vertex -2.338261 -2.486290 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.448950 -1.662151 23.000000
      vertex -1.517909 -1.609730 23.000000
      vertex -2.338261 -2.486290 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.448950 -1.662151 23.000000
      vertex -2.338261 -2.486290 23.000000
      vertex -2.175570 -2.618034 23.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex -2.000000 -2.732051 23.000000
      vertex -1.448950 -1.662151 23.000000
      vertex -2.175570 -2.618034 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.214023 -1.770840 23.000000
      vertex -1.813473 -2.827091 23.000000
      vertex -1.618034 -2.902113 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.214023 -1.770840 23.000000
      vertex -1.618034 -2.902113 23.000000
      vertex -1.415823 -2.956295 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.043311 -1.798827 23.000000
      vertex -1.214023 -1.770840 23.000000
      vertex -1.415823 -2.956295 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.043311 -1.798827 23.000000
      vertex -1.415823 -2.956295 23.000000
      vertex -1.209057 -2.989044 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.870574 -1.789461 23.000000
      vertex -1.043311 -1.798827 23.000000
      vertex -1.209057 -2.989044 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.870574 -1.789461 23.000000
      vertex -1.209057 -2.989044 23.000000
      vertex -1.000000 -3.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.703889 -1.743181 23.000000
      vertex -0.870574 -1.789461 23.000000
      vertex -1.000000 -3.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.703889 -1.743181 23.000000
      vertex -1.000000 -3.000000 23.000000
      vertex -0.100000 -3.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.551050 -1.662151 23.000000
      vertex -0.703889 -1.743181 23.000000
      vertex -0.100000 -3.000000 23.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex -0.551050 -1.662151 23.000000
      vertex -0.100000 -3.000000 23.000000
      vertex -0.419204 -1.550160 23.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex -0.625273 72.706810 23.000000
      vertex -0.100000 74.000000 23.000000
      vertex -0.785977 72.770844 23.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex -0.703889 71.256813 23.000000
      vertex -0.100000 71.099998 23.000000
      vertex -0.551050 71.337852 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.956689 72.798828 23.000000
      vertex -1.209057 73.989044 23.000000
      vertex -1.129426 72.789459 23.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex -0.956689 72.798828 23.000000
      vertex -0.785977 72.770844 23.000000
      vertex -0.100000 74.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex -0.956689 72.798828 23.000000
      vertex -0.100000 74.000000 23.000000
      vertex -1.000000 74.000000 23.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex -1.209057 73.989044 23.000000
      vertex -0.956689 72.798828 23.000000
      vertex -1.000000 74.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.204690 71.913506 23.000000
      vertex -0.241877 71.744560 23.000000
      vertex -0.100000 71.099998 23.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex -0.204690 71.913506 23.000000
      vertex -0.100000 71.099998 23.000000
      vertex -0.200000 72.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex -0.218704 72.171982 23.000000
      vertex -0.100000 74.000000 23.000000
      vertex -0.273940 72.335915 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.100000 71.099998 23.000000
      vertex -0.241877 71.744560 23.000000
      vertex -0.314514 71.587555 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.100000 71.099998 23.000000
      vertex -0.314514 71.587555 23.000000
      vertex -0.419204 71.449837 23.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex -0.551050 71.337852 23.000000
      vertex -0.100000 71.099998 23.000000
      vertex -0.419204 71.449837 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.100000 74.000000 23.000000
      vertex -0.625273 72.706810 23.000000
      vertex -0.482091 72.609734 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.100000 74.000000 23.000000
      vertex -0.482091 72.609734 23.000000
      vertex -0.363126 72.484146 23.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex -0.273940 72.335915 23.000000
      vertex -0.100000 74.000000 23.000000
      vertex -0.363126 72.484146 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 34.000000 71.099998 23.000000
      vertex 32.296108 71.256813 23.000000
      vertex 32.129425 71.210541 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 34.000000 71.099998 23.000000
      vertex 32.129425 71.210541 23.000000
      vertex 31.956688 71.201172 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.100000 71.099998 23.000000
      vertex 34.000000 71.099998 23.000000
      vertex 31.956688 71.201172 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.100000 71.099998 23.000000
      vertex 31.956688 71.201172 23.000000
      vertex -0.100000 74.000000 23.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex -0.200000 72.000000 23.000000
      vertex -0.100000 71.099998 23.000000
      vertex -0.100000 74.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex -0.200000 72.000000 23.000000
      vertex -0.100000 74.000000 23.000000
      vertex -0.218704 72.171982 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -3.000000 71.099998 23.000000
      vertex -1.636874 71.515862 23.000000
      vertex -1.726060 71.664085 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -3.000000 71.099998 23.000000
      vertex -1.726060 71.664085 23.000000
      vertex -1.781296 71.828026 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -3.000000 72.000000 23.000000
      vertex -3.000000 71.099998 23.000000
      vertex -1.781296 71.828026 23.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex -3.000000 72.000000 23.000000
      vertex -1.781296 71.828026 23.000000
      vertex -1.800000 72.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -2.989044 72.209061 23.000000
      vertex -3.000000 72.000000 23.000000
      vertex -1.800000 72.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -2.989044 72.209061 23.000000
      vertex -1.800000 72.000000 23.000000
      vertex -1.781296 72.171982 23.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex -1.781296 72.171982 23.000000
      vertex -1.726060 72.335915 23.000000
      vertex -2.902113 72.618034 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.781296 72.171982 23.000000
      vertex -2.902113 72.618034 23.000000
      vertex -2.956295 72.415825 23.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex -2.989044 72.209061 23.000000
      vertex -1.781296 72.171982 23.000000
      vertex -2.956295 72.415825 23.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex -1.726060 72.335915 23.000000
      vertex -1.636874 72.484146 23.000000
      vertex -2.732051 73.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.726060 72.335915 23.000000
      vertex -2.732051 73.000000 23.000000
      vertex -2.827091 72.813477 23.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex -2.902113 72.618034 23.000000
      vertex -1.726060 72.335915 23.000000
      vertex -2.827091 72.813477 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.100000 71.099998 23.000000
      vertex -0.703889 71.256813 23.000000
      vertex -0.870574 71.210541 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.100000 71.099998 23.000000
      vertex -0.870574 71.210541 23.000000
      vertex -1.043311 71.201172 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -3.000000 71.099998 23.000000
      vertex -0.100000 71.099998 23.000000
      vertex -1.043311 71.201172 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -3.000000 71.099998 23.000000
      vertex -1.043311 71.201172 23.000000
      vertex -1.214023 71.229156 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.374727 71.293190 23.000000
      vertex -3.000000 71.099998 23.000000
      vertex -1.214023 71.229156 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.129426 72.789459 23.000000
      vertex -1.209057 73.989044 23.000000
      vertex -1.415823 73.956299 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.129426 72.789459 23.000000
      vertex -1.415823 73.956299 23.000000
      vertex -1.618034 73.902115 23.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex -1.296111 72.743187 23.000000
      vertex -1.129426 72.789459 23.000000
      vertex -1.618034 73.902115 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -3.000000 71.099998 23.000000
      vertex -1.374727 71.293190 23.000000
      vertex -1.448950 71.337852 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -3.000000 71.099998 23.000000
      vertex -1.448950 71.337852 23.000000
      vertex -1.517909 71.390274 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.636874 71.515862 23.000000
      vertex -3.000000 71.099998 23.000000
      vertex -1.517909 71.390274 23.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex -1.636874 72.484146 23.000000
      vertex -1.517909 72.609734 23.000000
      vertex -2.486290 73.338264 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.636874 72.484146 23.000000
      vertex -2.486290 73.338264 23.000000
      vertex -2.618034 73.175575 23.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex -2.732051 73.000000 23.000000
      vertex -1.636874 72.484146 23.000000
      vertex -2.618034 73.175575 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.296111 72.743187 23.000000
      vertex -1.618034 73.902115 23.000000
      vertex -1.813473 73.827087 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.296111 72.743187 23.000000
      vertex -1.813473 73.827087 23.000000
      vertex -2.000000 73.732048 23.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex -1.448950 72.662155 23.000000
      vertex -1.296111 72.743187 23.000000
      vertex -2.000000 73.732048 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.448950 72.662155 23.000000
      vertex -2.000000 73.732048 23.000000
      vertex -2.175570 73.618034 23.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex -1.517909 72.609734 23.000000
      vertex -1.448950 72.662155 23.000000
      vertex -2.175570 73.618034 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.517909 72.609734 23.000000
      vertex -2.175570 73.618034 23.000000
      vertex -2.338261 73.486290 23.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex -2.486290 73.338264 23.000000
      vertex -1.517909 72.609734 23.000000
      vertex -2.338261 73.486290 23.000000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 28.000000 0.000000 -6.500000
      vertex 31.000000 0.000000 -10.500000
      vertex 28.000000 0.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 31.000000 0.000000 0.000000
      vertex 31.000000 0.000000 -10.500000
      vertex 28.000000 0.000000 -6.500000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 31.000000 0.000000 0.000000
      vertex 28.000000 0.000000 -6.500000
      vertex 28.000000 0.000000 -4.500000
    endloop
  endfacet
  facet normal -0.000000 1.000000 0.000000
    outer loop
      vertex 28.000000 0.000000 0.000000
      vertex 31.000000 0.000000 0.000000
      vertex 28.000000 0.000000 -4.500000
    endloop
  endfacet
  facet normal -0.000160 -0.790487 -0.612479
    outer loop
      vertex 9.043047 -2.641171 16.556952
      vertex 9.203295 -2.517043 16.396706
      vertex 19.224430 -2.618034 16.524431
    endloop
  endfacet
  facet normal 0.000166 -0.838590 -0.544762
    outer loop
      vertex 9.043047 -2.641171 16.556952
      vertex 19.224430 -2.618034 16.524431
      vertex 19.400002 -2.732051 16.699999
    endloop
  endfacet
  facet normal -0.000134 -0.848435 -0.529299
    outer loop
      vertex 8.871058 -2.748442 16.728943
      vertex 9.043047 -2.641171 16.556952
      vertex 19.400002 -2.732051 16.699999
    endloop
  endfacet
  facet normal 0.000139 -0.890951 -0.454099
    outer loop
      vertex 8.871058 -2.748442 16.728943
      vertex 19.400002 -2.732051 16.699999
      vertex 19.586525 -2.827091 16.886526
    endloop
  endfacet
  facet normal -0.000108 -0.897660 -0.440689
    outer loop
      vertex 8.689093 -2.837752 16.910908
      vertex 8.871058 -2.748442 16.728943
      vertex 19.586525 -2.827091 16.886526
    endloop
  endfacet
  facet normal 0.000111 -0.933544 -0.358464
    outer loop
      vertex 8.689093 -2.837752 16.910908
      vertex 19.586525 -2.827091 16.886526
      vertex 19.781965 -2.902113 17.081966
    endloop
  endfacet
  facet normal -0.000081 -0.937663 -0.347547
    outer loop
      vertex 8.499023 -2.908185 17.100977
      vertex 8.689093 -2.837752 16.910908
      vertex 19.781965 -2.902113 17.081966
    endloop
  endfacet
  facet normal 0.000084 -0.965905 -0.258896
    outer loop
      vertex 8.499023 -2.908185 17.100977
      vertex 19.781965 -2.902113 17.081966
      vertex 19.984177 -2.956295 17.284178
    endloop
  endfacet
  facet normal -0.000054 -0.968031 -0.250829
    outer loop
      vertex 8.302800 -2.959018 17.297199
      vertex 8.499023 -2.908185 17.100977
      vertex 19.984177 -2.956295 17.284178
    endloop
  endfacet
  facet normal 0.000056 -0.987680 -0.156489
    outer loop
      vertex 8.302800 -2.959018 17.297199
      vertex 19.984177 -2.956295 17.284178
      vertex 20.190943 -2.989044 17.490944
    endloop
  endfacet
  facet normal -0.000027 -0.988453 -0.151531
    outer loop
      vertex 8.102439 -2.989728 17.497561
      vertex 8.302800 -2.959018 17.297199
      vertex 20.190943 -2.989044 17.490944
    endloop
  endfacet
  facet normal 0.000028 -0.998628 -0.052365
    outer loop
      vertex 8.102439 -2.989728 17.497561
      vertex 20.190943 -2.989044 17.490944
      vertex 20.400002 -3.000000 17.699999
    endloop
  endfacet
  facet normal 0.000000 -0.998715 -0.050675
    outer loop
      vertex 7.900000 -3.000000 17.699999
      vertex 8.102439 -2.989728 17.497561
      vertex 20.400002 -3.000000 17.699999
    endloop
  endfacet
  facet normal 0.000822 -0.751404 -0.659842
    outer loop
      vertex 9.203295 -2.517043 16.396706
      vertex 9.237826 -2.486681 16.362173
      vertex 18.950329 -2.377843 16.250330
    endloop
  endfacet
  facet normal -0.000238 -0.716693 -0.697389
    outer loop
      vertex 9.203295 -2.517043 16.396706
      vertex 18.950329 -2.377843 16.250330
      vertex 19.061739 -2.486290 16.361740
    endloop
  endfacet
  facet normal 0.000192 -0.777053 -0.629435
    outer loop
      vertex 19.224430 -2.618034 16.524431
      vertex 9.203295 -2.517043 16.396706
      vertex 19.061739 -2.486290 16.361740
    endloop
  endfacet
  facet normal -0.000003 -0.716549 -0.697537
    outer loop
      vertex 18.950329 -2.377843 16.250330
      vertex 9.237826 -2.486681 16.362173
      vertex 9.350158 -2.377332 16.249844
    endloop
  endfacet
  facet normal 0.000001 -0.679079 -0.734066
    outer loop
      vertex 18.950329 -2.377843 16.250330
      vertex 9.350158 -2.377332 16.249844
      vertex 9.385835 -2.338767 16.214167
    endloop
  endfacet
  facet normal 0.000001 -0.679117 -0.734030
    outer loop
      vertex 18.913710 -2.338261 16.213709
      vertex 18.950329 -2.377843 16.250330
      vertex 9.385835 -2.338767 16.214167
    endloop
  endfacet
  facet normal -0.000003 -0.641029 -0.767517
    outer loop
      vertex 18.818363 -2.224103 16.118364
      vertex 18.913710 -2.338261 16.213709
      vertex 9.385835 -2.338767 16.214167
    endloop
  endfacet
  facet normal -0.000003 -0.641014 -0.767529
    outer loop
      vertex 18.818363 -2.224103 16.118364
      vertex 9.385835 -2.338767 16.214167
      vertex 9.482123 -2.223474 16.117878
    endloop
  endfacet
  facet normal 0.000001 -0.599986 -0.800010
    outer loop
      vertex 18.781965 -2.175570 16.081966
      vertex 18.818363 -2.224103 16.118364
      vertex 9.482123 -2.223474 16.117878
    endloop
  endfacet
  facet normal 0.000001 -0.599983 -0.800013
    outer loop
      vertex 18.781965 -2.175570 16.081966
      vertex 9.482123 -2.223474 16.117878
      vertex 9.517595 -2.176175 16.082405
    endloop
  endfacet
  facet normal -0.000003 -0.558516 -0.829494
    outer loop
      vertex 18.702162 -2.057048 16.002163
      vertex 18.781965 -2.175570 16.081966
      vertex 9.517595 -2.176175 16.082405
    endloop
  endfacet
  facet normal -0.000000 -0.558668 -0.829391
    outer loop
      vertex 18.702162 -2.057048 16.002163
      vertex 9.517595 -2.176175 16.082405
      vertex 9.597837 -2.057048 16.002163
    endloop
  endfacet
  facet normal 0.000000 -0.514342 -0.857585
    outer loop
      vertex 18.667950 -2.000000 15.967948
      vertex 18.702162 -2.057048 16.002163
      vertex 9.597837 -2.057048 16.002163
    endloop
  endfacet
  facet normal -0.000000 -0.514342 -0.857585
    outer loop
      vertex 18.667950 -2.000000 15.967948
      vertex 9.597837 -2.057048 16.002163
      vertex 9.632051 -2.000000 15.967948
    endloop
  endfacet
  facet normal 0.000000 -0.470208 -0.882556
    outer loop
      vertex 18.603889 -1.879764 15.903889
      vertex 18.667950 -2.000000 15.967948
      vertex 9.632051 -2.000000 15.967948
    endloop
  endfacet
  facet normal -0.000000 -0.470208 -0.882556
    outer loop
      vertex 18.603889 -1.879764 15.903889
      vertex 9.632051 -2.000000 15.967948
      vertex 9.696111 -1.879764 15.903889
    endloop
  endfacet
  facet normal -0.000000 -0.423384 -0.905950
    outer loop
      vertex 18.603889 -1.879764 15.903889
      vertex 9.696111 -1.879764 15.903889
      vertex 9.727091 -1.813473 15.872909
    endloop
  endfacet
  facet normal -0.000000 -0.423384 -0.905950
    outer loop
      vertex 18.572910 -1.813473 15.872909
      vertex 18.603889 -1.879764 15.903889
      vertex 9.727091 -1.813473 15.872909
    endloop
  endfacet
  facet normal -0.000000 -0.376922 -0.926245
    outer loop
      vertex 18.572910 -1.813473 15.872909
      vertex 9.727091 -1.813473 15.872909
      vertex 18.524063 -1.693444 15.824064
    endloop
  endfacet
  facet normal -0.000000 -0.279643 -0.960104
    outer loop
      vertex 18.463509 -1.500000 15.763508
      vertex 9.802114 -1.618034 15.797887
      vertex 9.836493 -1.500000 15.763508
    endloop
  endfacet
  facet normal -0.000000 -0.376922 -0.926245
    outer loop
      vertex 18.524063 -1.693444 15.824064
      vertex 9.727091 -1.813473 15.872909
      vertex 9.775936 -1.693444 15.824064
    endloop
  endfacet
  facet normal -0.000000 -0.327940 -0.944699
    outer loop
      vertex 18.524063 -1.693444 15.824064
      vertex 9.775936 -1.693444 15.824064
      vertex 9.802114 -1.618034 15.797887
    endloop
  endfacet
  facet normal -0.000000 -0.327939 -0.944699
    outer loop
      vertex 18.497887 -1.618034 15.797887
      vertex 18.524063 -1.693444 15.824064
      vertex 9.802114 -1.618034 15.797887
    endloop
  endfacet
  facet normal -0.000000 -0.279643 -0.960104
    outer loop
      vertex 18.497887 -1.618034 15.797887
      vertex 9.802114 -1.618034 15.797887
      vertex 18.463509 -1.500000 15.763508
    endloop
  endfacet
  facet normal -1.000000 0.000000 0.000000
    outer loop
      vertex 31.000000 0.000000 0.000000
      vertex 31.000000 71.000000 0.000000
      vertex 31.000000 71.000000 -10.500000
    endloop
  endfacet
  facet normal -1.000000 0.000000 0.000000
    outer loop
      vertex 31.000000 0.000000 0.000000
      vertex 31.000000 71.000000 -10.500000
      vertex 31.000000 0.000000 -10.500000
    endloop
  endfacet
  facet normal -1.000000 0.000000 0.000000
    outer loop
      vertex 18.400000 0.000000 15.500000
      vertex 18.400000 -0.000000 12.500000
      vertex 18.400000 -1.000000 12.500000
    endloop
  endfacet
  facet normal -1.000000 -0.000000 0.000000
    outer loop
      vertex 18.400000 0.000000 15.500000
      vertex 18.400000 -1.000000 12.500000
      vertex 18.400000 -1.000000 15.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 29.000000 2.000000 0.000000
      vertex 28.000000 0.000000 0.000000
      vertex 2.000000 2.000000 0.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 0.000000 0.000000 0.000000
      vertex 0.000000 39.500000 0.000000
      vertex 2.000000 39.500000 0.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 0.000000 0.000000 0.000000
      vertex 2.000000 39.500000 0.000000
      vertex 2.000000 2.000000 0.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.000000 0.000000 0.000000
      vertex 0.000000 0.000000 0.000000
      vertex 2.000000 2.000000 0.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.000000 0.000000 0.000000
      vertex 2.000000 2.000000 0.000000
      vertex 28.000000 0.000000 0.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.000000 -1.000000 0.000000
      vertex 3.000000 0.000000 0.000000
      vertex 28.000000 0.000000 0.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.000000 -1.000000 0.000000
      vertex 28.000000 0.000000 0.000000
      vertex 28.000000 -1.000000 0.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 2.000000 69.000000 0.000000
      vertex 2.000000 62.299999 0.000000
      vertex -0.000000 62.299999 0.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 2.000000 69.000000 0.000000
      vertex -0.000000 62.299999 0.000000
      vertex -0.000000 71.000000 0.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 29.000000 69.000000 0.000000
      vertex 2.000000 69.000000 0.000000
      vertex -0.000000 71.000000 0.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 29.000000 69.000000 0.000000
      vertex -0.000000 71.000000 0.000000
      vertex 31.000000 71.000000 0.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 29.000000 2.000000 0.000000
      vertex 29.000000 69.000000 0.000000
      vertex 31.000000 71.000000 0.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 29.000000 2.000000 0.000000
      vertex 31.000000 71.000000 0.000000
      vertex 31.000000 0.000000 0.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 28.000000 0.000000 0.000000
      vertex 29.000000 2.000000 0.000000
      vertex 31.000000 0.000000 0.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 2.000000 2.000000 2.000000
      vertex 2.000000 39.500000 2.000000
      vertex 0.000000 39.500000 2.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 2.000000 2.000000
      vertex 0.000000 39.500000 2.000000
      vertex 0.000000 0.000000 2.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 29.000000 2.000000 2.000000
      vertex 2.000000 2.000000 2.000000
      vertex 0.000000 0.000000 2.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 29.000000 2.000000 2.000000
      vertex 0.000000 0.000000 2.000000
      vertex 31.000000 0.000000 2.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 29.000000 69.000000 2.000000
      vertex 29.000000 2.000000 2.000000
      vertex 31.000000 0.000000 2.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 29.000000 69.000000 2.000000
      vertex 31.000000 0.000000 2.000000
      vertex 31.000000 71.000000 2.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 69.000000 2.000000
      vertex 29.000000 69.000000 2.000000
      vertex 31.000000 71.000000 2.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 2.000000 69.000000 2.000000
      vertex 31.000000 71.000000 2.000000
      vertex -0.000000 71.000000 2.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 2.000000 62.299999 2.000000
      vertex 2.000000 69.000000 2.000000
      vertex -0.000000 71.000000 2.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 62.299999 2.000000
      vertex -0.000000 71.000000 2.000000
      vertex 0.000000 62.299999 2.000000
    endloop
  endfacet
  facet normal 0.960104 -0.279643 0.000000
    outer loop
      vertex 9.802114 -1.618034 15.797887
      vertex 9.836493 -1.500000 15.500000
      vertex 9.836493 -1.500000 15.763508
    endloop
  endfacet
  facet normal 0.999657 -0.026176 0.000000
    outer loop
      vertex 9.897259 -1.104672 12.497259
      vertex 9.900000 -1.000000 12.500000
      vertex 9.900000 -1.000000 15.500000
    endloop
  endfacet
  facet normal 0.998629 -0.052334 0.000913
    outer loop
      vertex 9.897259 -1.104672 12.497259
      vertex 9.900000 -1.000000 15.500000
      vertex 9.889044 -1.209057 15.500000
    endloop
  endfacet
  facet normal 0.996918 -0.078456 0.000000
    outer loop
      vertex 9.889044 -1.209057 12.489044
      vertex 9.897259 -1.104672 12.497259
      vertex 9.889044 -1.209057 15.500000
    endloop
  endfacet
  facet normal 0.991445 -0.130526 0.000000
    outer loop
      vertex 9.875377 -1.312869 12.475377
      vertex 9.889044 -1.209057 12.489044
      vertex 9.889044 -1.209057 15.500000
    endloop
  endfacet
  facet normal 0.987687 -0.156437 0.000906
    outer loop
      vertex 9.875377 -1.312869 12.475377
      vertex 9.889044 -1.209057 15.500000
      vertex 9.856295 -1.415823 15.500000
    endloop
  endfacet
  facet normal 0.983254 -0.182241 0.000000
    outer loop
      vertex 9.856295 -1.415823 12.456295
      vertex 9.875377 -1.312869 12.475377
      vertex 9.856295 -1.415823 15.500000
    endloop
  endfacet
  facet normal 0.972370 -0.233446 0.000000
    outer loop
      vertex 9.831851 -1.517638 12.431851
      vertex 9.856295 -1.415823 12.456295
      vertex 9.856295 -1.415823 15.500000
    endloop
  endfacet
  facet normal 0.973428 -0.228994 -0.000156
    outer loop
      vertex 9.831851 -1.517638 12.431851
      vertex 9.856295 -1.415823 15.500000
      vertex 9.836493 -1.500000 15.500000
    endloop
  endfacet
  facet normal 0.958808 -0.284055 0.000182
    outer loop
      vertex 9.802114 -1.618034 12.402113
      vertex 9.831851 -1.517638 12.431851
      vertex 9.836493 -1.500000 15.500000
    endloop
  endfacet
  facet normal 0.960104 -0.279643 0.000000
    outer loop
      vertex 9.802114 -1.618034 12.402113
      vertex 9.836493 -1.500000 15.500000
      vertex 9.802114 -1.618034 15.797887
    endloop
  endfacet
  facet normal 0.942639 -0.333815 0.000000
    outer loop
      vertex 9.767160 -1.716736 12.367161
      vertex 9.802114 -1.618034 12.402113
      vertex 9.802114 -1.618034 15.797887
    endloop
  endfacet
  facet normal 0.944678 -0.327998 -0.000188
    outer loop
      vertex 9.767160 -1.716736 12.367161
      vertex 9.802114 -1.618034 15.797887
      vertex 9.775936 -1.693444 15.824064
    endloop
  endfacet
  facet normal 0.923847 -0.382763 0.000234
    outer loop
      vertex 9.727091 -1.813473 12.327091
      vertex 9.767160 -1.716736 12.367161
      vertex 9.775936 -1.693444 15.824064
    endloop
  endfacet
  facet normal 0.926243 -0.376928 0.000000
    outer loop
      vertex 9.727091 -1.813473 12.327091
      vertex 9.775936 -1.693444 15.824064
      vertex 9.727091 -1.813473 15.872909
    endloop
  endfacet
  facet normal 0.902584 -0.430514 0.000000
    outer loop
      vertex 9.682013 -1.907981 12.282013
      vertex 9.727091 -1.813473 12.327091
      vertex 9.727091 -1.813473 15.872909
    endloop
  endfacet
  facet normal 0.905910 -0.423471 -0.000227
    outer loop
      vertex 9.682013 -1.907981 12.282013
      vertex 9.727091 -1.813473 15.872909
      vertex 9.696111 -1.879764 15.903889
    endloop
  endfacet
  facet normal 0.878754 -0.477275 0.000298
    outer loop
      vertex 9.632051 -2.000000 12.232051
      vertex 9.682013 -1.907981 12.282013
      vertex 9.696111 -1.879764 15.903889
    endloop
  endfacet
  facet normal 0.882556 -0.470208 0.000000
    outer loop
      vertex 9.632051 -2.000000 12.232051
      vertex 9.696111 -1.879764 15.903889
      vertex 9.632051 -2.000000 15.967948
    endloop
  endfacet
  facet normal 0.852637 -0.522504 0.000000
    outer loop
      vertex 9.577341 -2.089278 12.177341
      vertex 9.632051 -2.000000 12.232051
      vertex 9.632051 -2.000000 15.967948
    endloop
  endfacet
  facet normal 0.857522 -0.514447 -0.000260
    outer loop
      vertex 9.577341 -2.089278 12.177341
      vertex 9.632051 -2.000000 15.967948
      vertex 9.597837 -2.057048 16.002163
    endloop
  endfacet
  facet normal 0.824012 -0.566573 0.000359
    outer loop
      vertex 9.518034 -2.175570 12.118034
      vertex 9.577341 -2.089278 12.177341
      vertex 9.597837 -2.057048 16.002163
    endloop
  endfacet
  facet normal 0.829394 -0.558665 0.000007
    outer loop
      vertex 9.518034 -2.175570 12.118034
      vertex 9.597837 -2.057048 16.002163
      vertex 9.517595 -2.176175 16.082405
    endloop
  endfacet
  facet normal 0.777150 -0.629316 -0.000010
    outer loop
      vertex 9.386290 -2.338261 11.986290
      vertex 9.518034 -2.175570 12.118034
      vertex 9.517595 -2.176175 16.082405
    endloop
  endfacet
  facet normal 0.799354 -0.600857 -0.001848
    outer loop
      vertex 9.386290 -2.338261 11.986290
      vertex 9.517595 -2.176175 16.082405
      vertex 9.482123 -2.223474 16.117878
    endloop
  endfacet
  facet normal 0.767531 -0.641012 0.000006
    outer loop
      vertex 9.386290 -2.338261 11.986290
      vertex 9.482123 -2.223474 16.117878
      vertex 9.385835 -2.338767 16.214167
    endloop
  endfacet
  facet normal 0.707112 -0.707102 -0.000008
    outer loop
      vertex 9.238261 -2.486290 11.838261
      vertex 9.386290 -2.338261 11.986290
      vertex 9.385835 -2.338767 16.214167
    endloop
  endfacet
  facet normal 0.733232 -0.679976 -0.001804
    outer loop
      vertex 9.238261 -2.486290 11.838261
      vertex 9.385835 -2.338767 16.214167
      vertex 9.350158 -2.377332 16.249844
    endloop
  endfacet
  facet normal 0.697532 -0.716554 0.000005
    outer loop
      vertex 9.238261 -2.486290 11.838261
      vertex 9.350158 -2.377332 16.249844
      vertex 9.237826 -2.486681 16.362173
    endloop
  endfacet
  facet normal 0.629325 -0.777142 -0.000007
    outer loop
      vertex 9.075571 -2.618034 11.675570
      vertex 9.238261 -2.486290 11.838261
      vertex 9.237826 -2.486681 16.362173
    endloop
  endfacet
  facet normal 0.659325 -0.751856 -0.001754
    outer loop
      vertex 9.075571 -2.618034 11.675570
      vertex 9.237826 -2.486681 16.362173
      vertex 9.203295 -2.517043 16.396706
    endloop
  endfacet
  facet normal 0.612584 -0.790405 0.000335
    outer loop
      vertex 9.075571 -2.618034 11.675570
      vertex 9.203295 -2.517043 16.396706
      vertex 9.043047 -2.641171 16.556952
    endloop
  endfacet
  facet normal 0.528848 -0.848717 -0.000499
    outer loop
      vertex 9.075571 -2.618034 11.675570
      vertex 9.043047 -2.641171 16.556952
      vertex 8.871058 -2.748442 16.728943
    endloop
  endfacet
  facet normal 0.544368 -0.838847 0.000384
    outer loop
      vertex 8.900000 -2.732051 11.500000
      vertex 9.075571 -2.618034 11.675570
      vertex 8.871058 -2.748442 16.728943
    endloop
  endfacet
  facet normal 0.440298 -0.897852 -0.000377
    outer loop
      vertex 8.900000 -2.732051 11.500000
      vertex 8.871058 -2.748442 16.728943
      vertex 8.689093 -2.837752 16.910908
    endloop
  endfacet
  facet normal 0.453770 -0.891119 0.000279
    outer loop
      vertex 8.713473 -2.827091 11.313473
      vertex 8.900000 -2.732051 11.500000
      vertex 8.689093 -2.837752 16.910908
    endloop
  endfacet
  facet normal 0.347235 -0.937778 -0.000274
    outer loop
      vertex 8.713473 -2.827091 11.313473
      vertex 8.689093 -2.837752 16.910908
      vertex 8.499023 -2.908185 17.100977
    endloop
  endfacet
  facet normal 0.358202 -0.933644 0.000191
    outer loop
      vertex 8.518034 -2.902113 11.118034
      vertex 8.713473 -2.827091 11.313473
      vertex 8.499023 -2.908185 17.100977
    endloop
  endfacet
  facet normal 0.250603 -0.968090 -0.000186
    outer loop
      vertex 8.518034 -2.902113 11.118034
      vertex 8.499023 -2.908185 17.100977
      vertex 8.302800 -2.959018 17.297199
    endloop
  endfacet
  facet normal 0.258710 -0.965955 0.000116
    outer loop
      vertex 8.315823 -2.956295 10.915823
      vertex 8.518034 -2.902113 11.118034
      vertex 8.302800 -2.959018 17.297199
    endloop
  endfacet
  facet normal 0.151395 -0.988473 -0.000113
    outer loop
      vertex 8.315823 -2.956295 10.915823
      vertex 8.302800 -2.959018 17.297199
      vertex 8.102439 -2.989728 17.497561
    endloop
  endfacet
  facet normal 0.156383 -0.987696 0.000053
    outer loop
      vertex 8.109057 -2.989044 10.709057
      vertex 8.315823 -2.956295 10.915823
      vertex 8.102439 -2.989728 17.497561
    endloop
  endfacet
  facet normal 0.050624 -0.998718 -0.000051
    outer loop
      vertex 8.109057 -2.989044 10.709057
      vertex 8.102439 -2.989728 17.497561
      vertex 7.900000 -3.000000 17.699999
    endloop
  endfacet
  facet normal 0.052336 -0.998629 0.000000
    outer loop
      vertex 7.900000 -3.000000 10.500000
      vertex 8.109057 -2.989044 10.709057
      vertex 7.900000 -3.000000 17.699999
    endloop
  endfacet
  facet normal 0.000000 -1.000000 0.000000
    outer loop
      vertex -0.000000 71.000000 0.000000
      vertex -0.000000 71.000000 -10.500000
      vertex 31.000000 71.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 0.000000
    outer loop
      vertex -0.000000 71.000000 0.000000
      vertex 31.000000 71.000000 -10.500000
      vertex 31.000000 71.000000 0.000000
    endloop
  endfacet
  facet normal 0.000000 1.000000 -0.000000
    outer loop
      vertex 3.000000 0.000000 -4.500000
      vertex 0.000000 0.000000 0.000000
      vertex 3.000000 0.000000 0.000000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 0.000000 0.000000 -10.500000
      vertex 0.000000 0.000000 0.000000
      vertex 3.000000 0.000000 -4.500000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 0.000000 0.000000 -10.500000
      vertex 3.000000 0.000000 -4.500000
      vertex 3.000000 0.000000 -6.500000
    endloop
  endfacet
  facet normal 0.000000 1.000000 -0.000000
    outer loop
      vertex 3.000000 0.000000 -10.500000
      vertex 0.000000 0.000000 -10.500000
      vertex 3.000000 0.000000 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 64.500000 13.000000
      vertex 4.764966 66.101761 13.000000
      vertex 4.635033 66.101761 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.000000 64.500000 13.000000
      vertex 21.471945 67.042038 13.000000
      vertex 21.437183 66.916840 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 64.500000 13.000000
      vertex 4.635033 66.101761 13.000000
      vertex 4.505862 66.115814 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 64.500000 13.000000
      vertex 4.505862 66.115814 13.000000
      vertex 4.378966 66.143745 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 4.255834 66.185226 13.000000
      vertex 2.000000 64.500000 13.000000
      vertex 4.378966 66.143745 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 64.500000 13.000000
      vertex 3.923136 66.385406 13.000000
      vertex 3.828805 66.474754 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 64.500000 13.000000
      vertex 3.828805 66.474754 13.000000
      vertex 3.744688 66.573792 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 3.671771 66.681335 13.000000
      vertex 2.000000 64.500000 13.000000
      vertex 3.744688 66.573792 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex 4.026576 68.293228 13.000000
      vertex 4.137910 68.360214 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex 4.137910 68.360214 13.000000
      vertex 4.255834 68.414772 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 4.378966 68.456261 13.000000
      vertex 2.000000 71.000000 13.000000
      vertex 4.255834 68.414772 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex 4.378966 68.456261 13.000000
      vertex 4.505862 68.484192 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex 4.505862 68.484192 13.000000
      vertex 4.635033 68.498238 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 4.764966 68.498238 13.000000
      vertex 2.000000 71.000000 13.000000
      vertex 4.635033 68.498238 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 20.105862 66.115814 13.000000
      vertex 5.262090 68.360214 13.000000
      vertex 5.373425 68.293228 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex 19.737911 66.239792 13.000000
      vertex 19.626575 66.306770 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex 19.626575 66.306770 13.000000
      vertex 19.523136 66.385406 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex 19.523136 66.385406 13.000000
      vertex 19.428804 66.474754 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 19.344688 66.573792 13.000000
      vertex 2.000000 71.000000 13.000000
      vertex 19.428804 66.474754 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.000000 71.000000 13.000000
      vertex 20.105862 68.484192 13.000000
      vertex 20.235033 68.498238 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.000000 71.000000 13.000000
      vertex 20.235033 68.498238 13.000000
      vertex 20.364965 68.498238 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 21.492966 67.170258 13.000000
      vertex 21.471945 67.042038 13.000000
      vertex 23.000000 64.500000 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.000000 64.500000 13.000000
      vertex 20.973425 66.306770 13.000000
      vertex 20.862089 66.239792 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.000000 64.500000 13.000000
      vertex 20.862089 66.239792 13.000000
      vertex 20.744165 66.185226 13.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 20.621033 66.143745 13.000000
      vertex 23.000000 64.500000 13.000000
      vertex 20.744165 66.185226 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 64.500000 13.000000
      vertex 4.255834 66.185226 13.000000
      vertex 4.137910 66.239792 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 64.500000 13.000000
      vertex 4.137910 66.239792 13.000000
      vertex 4.026576 66.306770 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 3.923136 66.385406 13.000000
      vertex 2.000000 64.500000 13.000000
      vertex 4.026576 66.306770 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 64.500000 13.000000
      vertex 3.671771 66.681335 13.000000
      vertex 3.610909 66.796135 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 64.500000 13.000000
      vertex 3.610909 66.796135 13.000000
      vertex 3.562816 66.916840 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 3.528055 67.042038 13.000000
      vertex 2.000000 64.500000 13.000000
      vertex 3.562816 66.916840 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 3.562816 67.683159 13.000000
      vertex 2.000000 71.000000 13.000000
      vertex 3.528055 67.557968 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex 3.744688 68.026207 13.000000
      vertex 3.828805 68.125244 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex 3.828805 68.125244 13.000000
      vertex 3.923136 68.214592 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 4.026576 68.293228 13.000000
      vertex 2.000000 71.000000 13.000000
      vertex 3.923136 68.214592 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex 4.764966 68.498238 13.000000
      vertex 4.894138 68.484192 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex 4.894138 68.484192 13.000000
      vertex 5.021034 68.456261 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 5.144166 68.414772 13.000000
      vertex 2.000000 71.000000 13.000000
      vertex 5.021034 68.456261 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 5.728229 67.918663 13.000000
      vertex 5.789091 67.803864 13.000000
      vertex 20.105862 66.115814 13.000000
    endloop
  endfacet
  facet normal -0.000000 -0.000000 1.000000
    outer loop
      vertex 5.728229 67.918663 13.000000
      vertex 20.105862 66.115814 13.000000
      vertex 5.655312 68.026207 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 5.144166 68.414772 13.000000
      vertex 5.262090 68.360214 13.000000
      vertex 20.105862 66.115814 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 5.144166 68.414772 13.000000
      vertex 20.105862 66.115814 13.000000
      vertex 19.978966 66.143745 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex 5.144166 68.414772 13.000000
      vertex 19.978966 66.143745 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex 19.978966 66.143745 13.000000
      vertex 19.855835 66.185226 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 19.737911 66.239792 13.000000
      vertex 2.000000 71.000000 13.000000
      vertex 19.855835 66.185226 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex 19.344688 68.026207 13.000000
      vertex 19.428804 68.125244 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex 19.428804 68.125244 13.000000
      vertex 19.523136 68.214592 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 19.626575 68.293228 13.000000
      vertex 2.000000 71.000000 13.000000
      vertex 19.523136 68.214592 13.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 21.171196 68.125244 13.000000
      vertex 21.255312 68.026207 13.000000
      vertex 23.000000 71.000000 13.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 21.171196 68.125244 13.000000
      vertex 23.000000 71.000000 13.000000
      vertex 21.076864 68.214592 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.000000 64.500000 13.000000
      vertex 21.437183 66.916840 13.000000
      vertex 21.389091 66.796135 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.000000 64.500000 13.000000
      vertex 21.389091 66.796135 13.000000
      vertex 21.328230 66.681335 13.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 21.255312 66.573792 13.000000
      vertex 23.000000 64.500000 13.000000
      vertex 21.328230 66.681335 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.000000 64.500000 13.000000
      vertex 21.255312 66.573792 13.000000
      vertex 21.171196 66.474754 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.000000 64.500000 13.000000
      vertex 21.171196 66.474754 13.000000
      vertex 21.076864 66.385406 13.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 20.973425 66.306770 13.000000
      vertex 23.000000 64.500000 13.000000
      vertex 21.076864 66.385406 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.000000 64.500000 13.000000
      vertex 5.571195 66.474754 13.000000
      vertex 5.476863 66.385406 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.000000 64.500000 13.000000
      vertex 5.476863 66.385406 13.000000
      vertex 5.373425 66.306770 13.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 5.262090 66.239792 13.000000
      vertex 23.000000 64.500000 13.000000
      vertex 5.373425 66.306770 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.000000 64.500000 13.000000
      vertex 5.262090 66.239792 13.000000
      vertex 5.144166 66.185226 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.000000 64.500000 13.000000
      vertex 5.144166 66.185226 13.000000
      vertex 5.021034 66.143745 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 64.500000 13.000000
      vertex 23.000000 64.500000 13.000000
      vertex 5.021034 66.143745 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 64.500000 13.000000
      vertex 5.021034 66.143745 13.000000
      vertex 4.894138 66.115814 13.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 4.764966 66.101761 13.000000
      vertex 2.000000 64.500000 13.000000
      vertex 4.894138 66.115814 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 64.500000 13.000000
      vertex 3.528055 67.042038 13.000000
      vertex 3.507034 67.170258 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 64.500000 13.000000
      vertex 3.507034 67.170258 13.000000
      vertex 3.500000 67.300003 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex 2.000000 64.500000 13.000000
      vertex 3.500000 67.300003 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex 3.500000 67.300003 13.000000
      vertex 3.507034 67.429741 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 3.528055 67.557968 13.000000
      vertex 2.000000 71.000000 13.000000
      vertex 3.507034 67.429741 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 20.105862 66.115814 13.000000
      vertex 5.373425 68.293228 13.000000
      vertex 5.476863 68.214592 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 20.105862 66.115814 13.000000
      vertex 5.476863 68.214592 13.000000
      vertex 5.571195 68.125244 13.000000
    endloop
  endfacet
  facet normal -0.000000 -0.000000 1.000000
    outer loop
      vertex 5.655312 68.026207 13.000000
      vertex 20.105862 66.115814 13.000000
      vertex 5.571195 68.125244 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 20.105862 66.115814 13.000000
      vertex 5.892965 67.429741 13.000000
      vertex 5.900000 67.300003 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 20.105862 66.115814 13.000000
      vertex 5.900000 67.300003 13.000000
      vertex 20.235033 66.101761 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex 19.626575 68.293228 13.000000
      vertex 19.737911 68.360214 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex 19.737911 68.360214 13.000000
      vertex 19.855835 68.414772 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.000000 71.000000 13.000000
      vertex 2.000000 71.000000 13.000000
      vertex 19.855835 68.414772 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.000000 71.000000 13.000000
      vertex 19.855835 68.414772 13.000000
      vertex 19.978966 68.456261 13.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 20.105862 68.484192 13.000000
      vertex 23.000000 71.000000 13.000000
      vertex 19.978966 68.456261 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.000000 71.000000 13.000000
      vertex 20.364965 68.498238 13.000000
      vertex 20.494139 68.484192 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.000000 71.000000 13.000000
      vertex 20.494139 68.484192 13.000000
      vertex 20.621033 68.456261 13.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 20.744165 68.414772 13.000000
      vertex 23.000000 71.000000 13.000000
      vertex 20.621033 68.456261 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.000000 71.000000 13.000000
      vertex 20.744165 68.414772 13.000000
      vertex 20.862089 68.360214 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.000000 71.000000 13.000000
      vertex 20.862089 68.360214 13.000000
      vertex 20.973425 68.293228 13.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 21.076864 68.214592 13.000000
      vertex 23.000000 71.000000 13.000000
      vertex 20.973425 68.293228 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.000000 71.000000 13.000000
      vertex 21.255312 68.026207 13.000000
      vertex 21.328230 67.918663 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.000000 71.000000 13.000000
      vertex 21.328230 67.918663 13.000000
      vertex 21.389091 67.803864 13.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 21.437183 67.683159 13.000000
      vertex 23.000000 71.000000 13.000000
      vertex 21.389091 67.803864 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.000000 64.500000 13.000000
      vertex 5.789091 66.796135 13.000000
      vertex 5.728229 66.681335 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.000000 64.500000 13.000000
      vertex 5.728229 66.681335 13.000000
      vertex 5.655312 66.573792 13.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 5.571195 66.474754 13.000000
      vertex 23.000000 64.500000 13.000000
      vertex 5.655312 66.573792 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex 3.562816 67.683159 13.000000
      vertex 3.610909 67.803864 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex 3.610909 67.803864 13.000000
      vertex 3.671771 67.918663 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 3.744688 68.026207 13.000000
      vertex 2.000000 71.000000 13.000000
      vertex 3.671771 67.918663 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 20.105862 66.115814 13.000000
      vertex 5.789091 67.803864 13.000000
      vertex 5.837184 67.683159 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 20.105862 66.115814 13.000000
      vertex 5.837184 67.683159 13.000000
      vertex 5.871944 67.557968 13.000000
    endloop
  endfacet
  facet normal -0.000000 -0.000000 1.000000
    outer loop
      vertex 5.892965 67.429741 13.000000
      vertex 20.105862 66.115814 13.000000
      vertex 5.871944 67.557968 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex 19.344688 66.573792 13.000000
      vertex 19.271770 66.681335 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex 19.271770 66.681335 13.000000
      vertex 19.210911 66.796135 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 19.162817 66.916840 13.000000
      vertex 2.000000 71.000000 13.000000
      vertex 19.210911 66.796135 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex 19.162817 66.916840 13.000000
      vertex 19.128056 67.042038 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex 19.128056 67.042038 13.000000
      vertex 19.107035 67.170258 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 19.099998 67.300003 13.000000
      vertex 2.000000 71.000000 13.000000
      vertex 19.107035 67.170258 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.000000 71.000000 13.000000
      vertex 21.437183 67.683159 13.000000
      vertex 21.471945 67.557968 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.000000 71.000000 13.000000
      vertex 21.471945 67.557968 13.000000
      vertex 21.492966 67.429741 13.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 23.000000 64.500000 13.000000
      vertex 23.000000 71.000000 13.000000
      vertex 21.492966 67.429741 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.000000 64.500000 13.000000
      vertex 21.492966 67.429741 13.000000
      vertex 21.500000 67.300003 13.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 21.492966 67.170258 13.000000
      vertex 23.000000 64.500000 13.000000
      vertex 21.500000 67.300003 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex 19.099998 67.300003 13.000000
      vertex 19.107035 67.429741 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex 19.107035 67.429741 13.000000
      vertex 19.128056 67.557968 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 19.162817 67.683159 13.000000
      vertex 2.000000 71.000000 13.000000
      vertex 19.128056 67.557968 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex 19.162817 67.683159 13.000000
      vertex 19.210911 67.803864 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 2.000000 71.000000 13.000000
      vertex 19.210911 67.803864 13.000000
      vertex 19.271770 67.918663 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 19.344688 68.026207 13.000000
      vertex 2.000000 71.000000 13.000000
      vertex 19.271770 67.918663 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.000000 64.500000 13.000000
      vertex 20.621033 66.143745 13.000000
      vertex 20.494139 66.115814 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.000000 64.500000 13.000000
      vertex 20.494139 66.115814 13.000000
      vertex 20.364965 66.101761 13.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 20.235033 66.101761 13.000000
      vertex 23.000000 64.500000 13.000000
      vertex 20.364965 66.101761 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 20.235033 66.101761 13.000000
      vertex 5.900000 67.300003 13.000000
      vertex 5.892965 67.170258 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 20.235033 66.101761 13.000000
      vertex 5.892965 67.170258 13.000000
      vertex 5.871944 67.042038 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.000000 64.500000 13.000000
      vertex 20.235033 66.101761 13.000000
      vertex 5.871944 67.042038 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 23.000000 64.500000 13.000000
      vertex 5.871944 67.042038 13.000000
      vertex 5.837184 66.916840 13.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 5.789091 66.796135 13.000000
      vertex 23.000000 64.500000 13.000000
      vertex 5.837184 66.916840 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 -1.000000 22.000000
      vertex -0.200000 -1.000000 22.000000
      vertex -0.218704 -0.828024 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 -1.000000 22.000000
      vertex -0.314514 -1.412443 22.000000
      vertex -0.241877 -1.255441 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 -1.000000 22.000000
      vertex -0.241877 -1.255441 22.000000
      vertex -0.204690 -1.086495 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.200000 -1.000000 22.000000
      vertex -1.000000 -1.000000 22.000000
      vertex -0.204690 -1.086495 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 -1.000000 22.000000
      vertex -0.703889 -1.743181 22.000000
      vertex -0.551050 -1.662151 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 -1.000000 22.000000
      vertex -0.551050 -1.662151 22.000000
      vertex -0.419204 -1.550160 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.314514 -1.412443 22.000000
      vertex -1.000000 -1.000000 22.000000
      vertex -0.419204 -1.550160 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 -1.000000 22.000000
      vertex -1.214023 -1.770840 22.000000
      vertex -1.043311 -1.798827 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 -1.000000 22.000000
      vertex -1.043311 -1.798827 22.000000
      vertex -0.870574 -1.789461 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.703889 -1.743181 22.000000
      vertex -1.000000 -1.000000 22.000000
      vertex -0.870574 -1.789461 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 -1.000000 22.000000
      vertex -1.517909 -1.609730 22.000000
      vertex -1.448950 -1.662151 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 -1.000000 22.000000
      vertex -1.448950 -1.662151 22.000000
      vertex -1.374727 -1.706810 22.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex -1.214023 -1.770840 22.000000
      vertex -1.000000 -1.000000 22.000000
      vertex -1.374727 -1.706810 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 -1.000000 22.000000
      vertex -1.781296 -1.171976 22.000000
      vertex -1.726060 -1.335911 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 -1.000000 22.000000
      vertex -1.726060 -1.335911 22.000000
      vertex -1.636874 -1.484139 22.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex -1.517909 -1.609730 22.000000
      vertex -1.000000 -1.000000 22.000000
      vertex -1.636874 -1.484139 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 -1.000000 22.000000
      vertex -1.726060 -0.664089 22.000000
      vertex -1.781296 -0.828024 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 -1.000000 22.000000
      vertex -1.781296 -0.828024 22.000000
      vertex -1.800000 -1.000000 22.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex -1.781296 -1.171976 22.000000
      vertex -1.000000 -1.000000 22.000000
      vertex -1.800000 -1.000000 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 -1.000000 22.000000
      vertex -1.448950 -0.337849 22.000000
      vertex -1.517909 -0.390270 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 -1.000000 22.000000
      vertex -1.517909 -0.390270 22.000000
      vertex -1.636874 -0.515861 22.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex -1.726060 -0.664089 22.000000
      vertex -1.000000 -1.000000 22.000000
      vertex -1.636874 -0.515861 22.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex -1.000000 -1.000000 22.000000
      vertex -0.956689 -0.201173 22.000000
      vertex -1.129426 -0.210539 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 -1.000000 22.000000
      vertex -1.129426 -0.210539 22.000000
      vertex -1.296111 -0.256819 22.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex -1.448950 -0.337849 22.000000
      vertex -1.000000 -1.000000 22.000000
      vertex -1.296111 -0.256819 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 -1.000000 22.000000
      vertex -0.482091 -0.390270 22.000000
      vertex -0.625273 -0.293190 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 -1.000000 22.000000
      vertex -0.625273 -0.293190 22.000000
      vertex -0.785977 -0.229160 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.956689 -0.201173 22.000000
      vertex -1.000000 -1.000000 22.000000
      vertex -0.785977 -0.229160 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 -1.000000 22.000000
      vertex -0.218704 -0.828024 22.000000
      vertex -0.273940 -0.664089 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 -1.000000 22.000000
      vertex -0.273940 -0.664089 22.000000
      vertex -0.363126 -0.515861 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.482091 -0.390270 22.000000
      vertex -1.000000 -1.000000 22.000000
      vertex -0.363126 -0.515861 22.000000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex -1.500000 8.000000 16.000000
      vertex -1.500000 8.000000 20.500000
      vertex 0.000000 8.000000 20.500000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex -1.500000 8.000000 16.000000
      vertex 0.000000 8.000000 20.500000
      vertex 0.000000 8.000000 16.000000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 0.000000
    outer loop
      vertex 23.250000 -3.000000 -3.500000
      vertex 20.400002 -3.000000 10.500000
      vertex 8.250000 -3.000000 -3.500000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 0.000000
    outer loop
      vertex 7.900000 -3.000000 17.699999
      vertex 20.400002 -3.000000 17.699999
      vertex 32.000000 -3.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 0.000000
    outer loop
      vertex 7.900000 -3.000000 17.699999
      vertex 32.000000 -3.000000 23.000000
      vertex -0.100000 -3.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 0.000000
    outer loop
      vertex 7.900000 -3.000000 10.500000
      vertex 7.900000 -3.000000 17.699999
      vertex -0.100000 -3.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 0.000000
    outer loop
      vertex 7.900000 -3.000000 10.500000
      vertex -0.100000 -3.000000 23.000000
      vertex -1.000000 -3.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 0.000000
    outer loop
      vertex -1.000000 -3.000000 -10.500000
      vertex 7.900000 -3.000000 10.500000
      vertex -1.000000 -3.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 0.000000
    outer loop
      vertex 8.250000 -3.000000 -3.500000
      vertex 20.400002 -3.000000 10.500000
      vertex 7.900000 -3.000000 10.500000
    endloop
  endfacet
  facet normal -0.000000 -1.000000 0.000000
    outer loop
      vertex 8.250000 -3.000000 -3.500000
      vertex 7.900000 -3.000000 10.500000
      vertex -1.000000 -3.000000 -10.500000
    endloop
  endfacet
  facet normal -0.000000 -1.000000 0.000000
    outer loop
      vertex 8.250000 -3.000000 -7.000000
      vertex 8.250000 -3.000000 -3.500000
      vertex -1.000000 -3.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 0.000000
    outer loop
      vertex 8.250000 -3.000000 -7.000000
      vertex -1.000000 -3.000000 -10.500000
      vertex -0.100000 -3.000000 -10.500000
    endloop
  endfacet
  facet normal -0.000000 -1.000000 0.000000
    outer loop
      vertex 23.250000 -3.000000 -7.000000
      vertex 8.250000 -3.000000 -7.000000
      vertex -0.100000 -3.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 -0.000000
    outer loop
      vertex 23.250000 -3.000000 -7.000000
      vertex -0.100000 -3.000000 -10.500000
      vertex 32.000000 -3.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 0.000000
    outer loop
      vertex 23.250000 -3.000000 -3.500000
      vertex 23.250000 -3.000000 -7.000000
      vertex 32.000000 -3.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 0.000000
    outer loop
      vertex 23.250000 -3.000000 -3.500000
      vertex 32.000000 -3.000000 -10.500000
      vertex 32.000000 -3.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 0.000000
    outer loop
      vertex 20.400002 -3.000000 10.500000
      vertex 23.250000 -3.000000 -3.500000
      vertex 32.000000 -3.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 0.000000
    outer loop
      vertex 20.400002 -3.000000 10.500000
      vertex 32.000000 -3.000000 23.000000
      vertex 20.400002 -3.000000 17.699999
    endloop
  endfacet
  facet normal 1.000000 0.000000 0.000000
    outer loop
      vertex 23.000000 71.000000 13.000000
      vertex 23.000000 64.500000 13.000000
      vertex 23.000000 64.500000 11.000000
    endloop
  endfacet
  facet normal 1.000000 0.000000 0.000000
    outer loop
      vertex 23.000000 71.000000 13.000000
      vertex 23.000000 64.500000 11.000000
      vertex 23.000000 71.000000 11.000000
    endloop
  endfacet
  facet normal -1.000000 0.000000 0.000000
    outer loop
      vertex 28.000000 0.000000 -4.500000
      vertex 28.000000 -1.000000 -4.500000
      vertex 28.000000 -1.000000 0.000000
    endloop
  endfacet
  facet normal -1.000000 0.000000 0.000000
    outer loop
      vertex 28.000000 0.000000 -4.500000
      vertex 28.000000 -1.000000 0.000000
      vertex 28.000000 0.000000 0.000000
    endloop
  endfacet
  facet normal -0.994138 -0.108118 0.000000
    outer loop
      vertex 32.781296 -0.828024 22.000000
      vertex 32.799999 -1.000000 22.000000
      vertex 32.799999 -1.000000 23.000000
    endloop
  endfacet
  facet normal -0.994138 -0.108118 0.000000
    outer loop
      vertex 32.781296 -0.828024 22.000000
      vertex 32.799999 -1.000000 23.000000
      vertex 32.781296 -0.828024 23.000000
    endloop
  endfacet
  facet normal -0.947652 -0.319305 0.000000
    outer loop
      vertex 32.726059 -0.664089 22.000000
      vertex 32.781296 -0.828024 22.000000
      vertex 32.781296 -0.828024 23.000000
    endloop
  endfacet
  facet normal -0.947652 -0.319305 0.000000
    outer loop
      vertex 32.726059 -0.664089 22.000000
      vertex 32.781296 -0.828024 23.000000
      vertex 32.726059 -0.664089 23.000000
    endloop
  endfacet
  facet normal -0.856863 -0.515545 0.000000
    outer loop
      vertex 32.636875 -0.515861 22.000000
      vertex 32.726059 -0.664089 22.000000
      vertex 32.726059 -0.664089 23.000000
    endloop
  endfacet
  facet normal -0.856863 -0.515545 0.000000
    outer loop
      vertex 32.636875 -0.515861 22.000000
      vertex 32.726059 -0.664089 23.000000
      vertex 32.636875 -0.515861 23.000000
    endloop
  endfacet
  facet normal -0.725996 -0.687699 0.000000
    outer loop
      vertex 32.517910 -0.390270 22.000000
      vertex 32.636875 -0.515861 22.000000
      vertex 32.636875 -0.515861 23.000000
    endloop
  endfacet
  facet normal -0.725996 -0.687699 0.000000
    outer loop
      vertex 32.517910 -0.390270 22.000000
      vertex 32.636875 -0.515861 23.000000
      vertex 32.517910 -0.390270 23.000000
    endloop
  endfacet
  facet normal -0.561191 -0.827686 0.000000
    outer loop
      vertex 32.374729 -0.293190 22.000000
      vertex 32.517910 -0.390270 22.000000
      vertex 32.517910 -0.390270 23.000000
    endloop
  endfacet
  facet normal -0.561191 -0.827686 0.000000
    outer loop
      vertex 32.374729 -0.293190 22.000000
      vertex 32.517910 -0.390270 23.000000
      vertex 32.374729 -0.293190 23.000000
    endloop
  endfacet
  facet normal -0.370135 -0.928978 0.000000
    outer loop
      vertex 32.214024 -0.229160 22.000000
      vertex 32.374729 -0.293190 22.000000
      vertex 32.374729 -0.293190 23.000000
    endloop
  endfacet
  facet normal -0.370135 -0.928978 0.000000
    outer loop
      vertex 32.214024 -0.229160 22.000000
      vertex 32.374729 -0.293190 23.000000
      vertex 32.214024 -0.229160 23.000000
    endloop
  endfacet
  facet normal -0.161782 -0.986827 0.000000
    outer loop
      vertex 32.043312 -0.201173 22.000000
      vertex 32.214024 -0.229160 22.000000
      vertex 32.214024 -0.229160 23.000000
    endloop
  endfacet
  facet normal -0.161782 -0.986827 0.000000
    outer loop
      vertex 32.043312 -0.201173 22.000000
      vertex 32.214024 -0.229160 23.000000
      vertex 32.043312 -0.201173 23.000000
    endloop
  endfacet
  facet normal 0.054138 -0.998533 0.000000
    outer loop
      vertex 31.870573 -0.210539 22.000000
      vertex 32.043312 -0.201173 22.000000
      vertex 32.043312 -0.201173 23.000000
    endloop
  endfacet
  facet normal 0.054138 -0.998533 0.000000
    outer loop
      vertex 31.870573 -0.210539 22.000000
      vertex 32.043312 -0.201173 23.000000
      vertex 31.870573 -0.210539 23.000000
    endloop
  endfacet
  facet normal 0.267531 -0.963549 0.000000
    outer loop
      vertex 31.703890 -0.256819 22.000000
      vertex 31.870573 -0.210539 22.000000
      vertex 31.870573 -0.210539 23.000000
    endloop
  endfacet
  facet normal 0.267531 -0.963549 0.000000
    outer loop
      vertex 31.703890 -0.256819 22.000000
      vertex 31.870573 -0.210539 23.000000
      vertex 31.703890 -0.256819 23.000000
    endloop
  endfacet
  facet normal 0.468412 -0.883510 0.000000
    outer loop
      vertex 31.551052 -0.337849 22.000000
      vertex 31.703890 -0.256819 22.000000
      vertex 31.703890 -0.256819 23.000000
    endloop
  endfacet
  facet normal 0.468412 -0.883510 0.000000
    outer loop
      vertex 31.551052 -0.337849 22.000000
      vertex 31.703890 -0.256819 23.000000
      vertex 31.551052 -0.337849 23.000000
    endloop
  endfacet
  facet normal 0.605159 -0.796104 0.000000
    outer loop
      vertex 31.482090 -0.390270 22.000000
      vertex 31.551052 -0.337849 22.000000
      vertex 31.551052 -0.337849 23.000000
    endloop
  endfacet
  facet normal 0.605159 -0.796104 0.000000
    outer loop
      vertex 31.482090 -0.390270 22.000000
      vertex 31.551052 -0.337849 23.000000
      vertex 31.482090 -0.390270 23.000000
    endloop
  endfacet
  facet normal 0.726002 -0.687693 0.000000
    outer loop
      vertex 31.363127 -0.515861 22.000000
      vertex 31.482090 -0.390270 22.000000
      vertex 31.482090 -0.390270 23.000000
    endloop
  endfacet
  facet normal 0.726002 -0.687693 0.000000
    outer loop
      vertex 31.363127 -0.515861 22.000000
      vertex 31.482090 -0.390270 23.000000
      vertex 31.363127 -0.515861 23.000000
    endloop
  endfacet
  facet normal 0.856853 -0.515561 0.000000
    outer loop
      vertex 31.273939 -0.664089 22.000000
      vertex 31.363127 -0.515861 22.000000
      vertex 31.363127 -0.515861 23.000000
    endloop
  endfacet
  facet normal 0.856853 -0.515561 0.000000
    outer loop
      vertex 31.273939 -0.664089 22.000000
      vertex 31.363127 -0.515861 23.000000
      vertex 31.273939 -0.664089 23.000000
    endloop
  endfacet
  facet normal 0.947655 -0.319295 0.000000
    outer loop
      vertex 31.218704 -0.828024 22.000000
      vertex 31.273939 -0.664089 22.000000
      vertex 31.273939 -0.664089 23.000000
    endloop
  endfacet
  facet normal 0.947655 -0.319295 0.000000
    outer loop
      vertex 31.218704 -0.828024 22.000000
      vertex 31.273939 -0.664089 23.000000
      vertex 31.218704 -0.828024 23.000000
    endloop
  endfacet
  facet normal 0.994137 -0.108129 0.000000
    outer loop
      vertex 31.199999 -1.000000 22.000000
      vertex 31.218704 -0.828024 22.000000
      vertex 31.218704 -0.828024 23.000000
    endloop
  endfacet
  facet normal 0.994137 -0.108129 0.000000
    outer loop
      vertex 31.199999 -1.000000 22.000000
      vertex 31.218704 -0.828024 23.000000
      vertex 31.199999 -1.000000 23.000000
    endloop
  endfacet
  facet normal 0.994137 0.108129 0.000000
    outer loop
      vertex 31.218704 -1.171976 22.000000
      vertex 31.199999 -1.000000 22.000000
      vertex 31.199999 -1.000000 23.000000
    endloop
  endfacet
  facet normal 0.994137 0.108129 -0.000000
    outer loop
      vertex 31.218704 -1.171976 22.000000
      vertex 31.199999 -1.000000 23.000000
      vertex 31.218704 -1.171976 23.000000
    endloop
  endfacet
  facet normal 0.947655 0.319295 0.000000
    outer loop
      vertex 31.273939 -1.335911 22.000000
      vertex 31.218704 -1.171976 22.000000
      vertex 31.218704 -1.171976 23.000000
    endloop
  endfacet
  facet normal 0.947655 0.319295 -0.000000
    outer loop
      vertex 31.273939 -1.335911 22.000000
      vertex 31.218704 -1.171976 23.000000
      vertex 31.273939 -1.335911 23.000000
    endloop
  endfacet
  facet normal 0.856852 0.515562 0.000000
    outer loop
      vertex 31.363127 -1.484139 22.000000
      vertex 31.273939 -1.335911 22.000000
      vertex 31.273939 -1.335911 23.000000
    endloop
  endfacet
  facet normal 0.856852 0.515562 -0.000000
    outer loop
      vertex 31.363127 -1.484139 22.000000
      vertex 31.273939 -1.335911 23.000000
      vertex 31.363127 -1.484139 23.000000
    endloop
  endfacet
  facet normal 0.726002 0.687693 0.000000
    outer loop
      vertex 31.482090 -1.609730 22.000000
      vertex 31.363127 -1.484139 22.000000
      vertex 31.363127 -1.484139 23.000000
    endloop
  endfacet
  facet normal 0.726002 0.687693 -0.000000
    outer loop
      vertex 31.482090 -1.609730 22.000000
      vertex 31.363127 -1.484139 23.000000
      vertex 31.482090 -1.609730 23.000000
    endloop
  endfacet
  facet normal 0.605159 0.796104 0.000000
    outer loop
      vertex 31.551052 -1.662151 22.000000
      vertex 31.482090 -1.609730 22.000000
      vertex 31.482090 -1.609730 23.000000
    endloop
  endfacet
  facet normal 0.605159 0.796104 -0.000000
    outer loop
      vertex 31.551052 -1.662151 22.000000
      vertex 31.482090 -1.609730 23.000000
      vertex 31.551052 -1.662151 23.000000
    endloop
  endfacet
  facet normal 0.515555 0.856856 0.000000
    outer loop
      vertex 31.625275 -1.706810 22.000000
      vertex 31.551052 -1.662151 22.000000
      vertex 31.551052 -1.662151 23.000000
    endloop
  endfacet
  facet normal 0.515555 0.856856 -0.000000
    outer loop
      vertex 31.625275 -1.706810 22.000000
      vertex 31.551052 -1.662151 23.000000
      vertex 31.625275 -1.706810 23.000000
    endloop
  endfacet
  facet normal 0.370143 0.928975 0.000000
    outer loop
      vertex 31.785976 -1.770840 22.000000
      vertex 31.625275 -1.706810 22.000000
      vertex 31.625275 -1.706810 23.000000
    endloop
  endfacet
  facet normal 0.370143 0.928975 -0.000000
    outer loop
      vertex 31.785976 -1.770840 22.000000
      vertex 31.625275 -1.706810 23.000000
      vertex 31.785976 -1.770840 23.000000
    endloop
  endfacet
  facet normal 0.161782 0.986827 0.000000
    outer loop
      vertex 31.956688 -1.798827 22.000000
      vertex 31.785976 -1.770840 22.000000
      vertex 31.785976 -1.770840 23.000000
    endloop
  endfacet
  facet normal 0.161782 0.986827 -0.000000
    outer loop
      vertex 31.956688 -1.798827 22.000000
      vertex 31.785976 -1.770840 23.000000
      vertex 31.956688 -1.798827 23.000000
    endloop
  endfacet
  facet normal -0.054138 0.998533 0.000000
    outer loop
      vertex 32.129425 -1.789461 22.000000
      vertex 31.956688 -1.798827 22.000000
      vertex 31.956688 -1.798827 23.000000
    endloop
  endfacet
  facet normal -0.054138 0.998533 0.000000
    outer loop
      vertex 32.129425 -1.789461 22.000000
      vertex 31.956688 -1.798827 23.000000
      vertex 32.129425 -1.789461 23.000000
    endloop
  endfacet
  facet normal -0.267531 0.963549 0.000000
    outer loop
      vertex 32.296108 -1.743181 22.000000
      vertex 32.129425 -1.789461 22.000000
      vertex 32.129425 -1.789461 23.000000
    endloop
  endfacet
  facet normal -0.267531 0.963549 0.000000
    outer loop
      vertex 32.296108 -1.743181 22.000000
      vertex 32.129425 -1.789461 23.000000
      vertex 32.296108 -1.743181 23.000000
    endloop
  endfacet
  facet normal -0.468398 0.883518 0.000000
    outer loop
      vertex 32.448952 -1.662151 22.000000
      vertex 32.296108 -1.743181 22.000000
      vertex 32.296108 -1.743181 23.000000
    endloop
  endfacet
  facet normal -0.468398 0.883518 0.000000
    outer loop
      vertex 32.448952 -1.662151 22.000000
      vertex 32.296108 -1.743181 23.000000
      vertex 32.448952 -1.662151 23.000000
    endloop
  endfacet
  facet normal -0.647395 0.762154 0.000000
    outer loop
      vertex 32.580795 -1.550160 22.000000
      vertex 32.448952 -1.662151 22.000000
      vertex 32.448952 -1.662151 23.000000
    endloop
  endfacet
  facet normal -0.647395 0.762154 0.000000
    outer loop
      vertex 32.580795 -1.550160 22.000000
      vertex 32.448952 -1.662151 23.000000
      vertex 32.580795 -1.550160 23.000000
    endloop
  endfacet
  facet normal -0.796090 0.605179 0.000000
    outer loop
      vertex 32.685486 -1.412443 22.000000
      vertex 32.580795 -1.550160 22.000000
      vertex 32.580795 -1.550160 23.000000
    endloop
  endfacet
  facet normal -0.796090 0.605179 0.000000
    outer loop
      vertex 32.685486 -1.412443 22.000000
      vertex 32.580795 -1.550160 23.000000
      vertex 32.685486 -1.412443 23.000000
    endloop
  endfacet
  facet normal -0.907570 0.419902 0.000000
    outer loop
      vertex 32.758125 -1.255441 22.000000
      vertex 32.685486 -1.412443 22.000000
      vertex 32.685486 -1.412443 23.000000
    endloop
  endfacet
  facet normal -0.907570 0.419902 0.000000
    outer loop
      vertex 32.758125 -1.255441 22.000000
      vertex 32.685486 -1.412443 23.000000
      vertex 32.758125 -1.255441 23.000000
    endloop
  endfacet
  facet normal -0.976623 0.214959 0.000000
    outer loop
      vertex 32.795311 -1.086495 22.000000
      vertex 32.758125 -1.255441 22.000000
      vertex 32.758125 -1.255441 23.000000
    endloop
  endfacet
  facet normal -0.976623 0.214959 0.000000
    outer loop
      vertex 32.795311 -1.086495 22.000000
      vertex 32.758125 -1.255441 23.000000
      vertex 32.795311 -1.086495 23.000000
    endloop
  endfacet
  facet normal -0.998534 0.054123 0.000000
    outer loop
      vertex 32.799999 -1.000000 22.000000
      vertex 32.795311 -1.086495 22.000000
      vertex 32.795311 -1.086495 23.000000
    endloop
  endfacet
  facet normal -0.998534 0.054123 0.000000
    outer loop
      vertex 32.799999 -1.000000 22.000000
      vertex 32.795311 -1.086495 23.000000
      vertex 32.799999 -1.000000 23.000000
    endloop
  endfacet
  facet normal -0.052336 -0.998630 0.000000
    outer loop
      vertex 20.190943 -2.989044 17.490944
      vertex 20.400002 -3.000000 10.500000
      vertex 20.400002 -3.000000 17.699999
    endloop
  endfacet
  facet normal -0.052336 -0.998630 0.000000
    outer loop
      vertex 20.190943 -2.989044 10.709057
      vertex 20.400002 -3.000000 10.500000
      vertex 20.190943 -2.989044 17.490944
    endloop
  endfacet
  facet normal -0.156434 -0.987688 0.000000
    outer loop
      vertex 20.190943 -2.989044 10.709057
      vertex 20.190943 -2.989044 17.490944
      vertex 19.984177 -2.956295 17.284178
    endloop
  endfacet
  facet normal -0.156434 -0.987688 0.000000
    outer loop
      vertex 19.984177 -2.956295 10.915823
      vertex 20.190943 -2.989044 10.709057
      vertex 19.984177 -2.956295 17.284178
    endloop
  endfacet
  facet normal -0.258818 -0.965926 0.000000
    outer loop
      vertex 19.984177 -2.956295 10.915823
      vertex 19.984177 -2.956295 17.284178
      vertex 19.781965 -2.902113 17.081966
    endloop
  endfacet
  facet normal -0.258818 -0.965926 0.000000
    outer loop
      vertex 19.781965 -2.902113 11.118034
      vertex 19.984177 -2.956295 10.915823
      vertex 19.781965 -2.902113 17.081966
    endloop
  endfacet
  facet normal -0.358367 -0.933581 0.000000
    outer loop
      vertex 19.781965 -2.902113 11.118034
      vertex 19.781965 -2.902113 17.081966
      vertex 19.586525 -2.827091 16.886526
    endloop
  endfacet
  facet normal -0.358367 -0.933581 0.000000
    outer loop
      vertex 19.586525 -2.827091 11.313473
      vertex 19.781965 -2.902113 11.118034
      vertex 19.586525 -2.827091 16.886526
    endloop
  endfacet
  facet normal -0.453997 -0.891003 0.000000
    outer loop
      vertex 19.586525 -2.827091 11.313473
      vertex 19.586525 -2.827091 16.886526
      vertex 19.400002 -2.732051 16.699999
    endloop
  endfacet
  facet normal -0.453997 -0.891003 0.000000
    outer loop
      vertex 19.400002 -2.732051 11.500000
      vertex 19.586525 -2.827091 11.313473
      vertex 19.400002 -2.732051 16.699999
    endloop
  endfacet
  facet normal -0.544638 -0.838672 0.000000
    outer loop
      vertex 19.400002 -2.732051 11.500000
      vertex 19.400002 -2.732051 16.699999
      vertex 19.224430 -2.618034 16.524431
    endloop
  endfacet
  facet normal -0.544638 -0.838671 0.000000
    outer loop
      vertex 19.224430 -2.618034 11.675570
      vertex 19.400002 -2.732051 11.500000
      vertex 19.224430 -2.618034 16.524431
    endloop
  endfacet
  facet normal -0.629319 -0.777147 0.000000
    outer loop
      vertex 19.224430 -2.618034 11.675570
      vertex 19.224430 -2.618034 16.524431
      vertex 19.061739 -2.486290 16.361740
    endloop
  endfacet
  facet normal -0.629319 -0.777147 0.000000
    outer loop
      vertex 19.061739 -2.486290 11.838261
      vertex 19.224430 -2.618034 11.675570
      vertex 19.061739 -2.486290 16.361740
    endloop
  endfacet
  facet normal -0.697511 -0.716574 0.000000
    outer loop
      vertex 19.061739 -2.486290 11.838261
      vertex 19.061739 -2.486290 16.361740
      vertex 18.950329 -2.377843 16.250330
    endloop
  endfacet
  facet normal -0.707348 -0.706865 -0.000487
    outer loop
      vertex 18.913710 -2.338261 11.986290
      vertex 19.061739 -2.486290 11.838261
      vertex 18.950329 -2.377843 16.250330
    endloop
  endfacet
  facet normal -0.734048 -0.679098 0.000000
    outer loop
      vertex 18.913710 -2.338261 11.986290
      vertex 18.950329 -2.377843 16.250330
      vertex 18.913710 -2.338261 16.213709
    endloop
  endfacet
  facet normal -0.767512 -0.641035 0.000000
    outer loop
      vertex 18.913710 -2.338261 11.986290
      vertex 18.913710 -2.338261 16.213709
      vertex 18.818363 -2.224103 16.118364
    endloop
  endfacet
  facet normal -0.777367 -0.629047 -0.000559
    outer loop
      vertex 18.781965 -2.175570 12.118034
      vertex 18.913710 -2.338261 11.986290
      vertex 18.818363 -2.224103 16.118364
    endloop
  endfacet
  facet normal -0.800010 -0.599987 0.000000
    outer loop
      vertex 18.781965 -2.175570 12.118034
      vertex 18.818363 -2.224103 16.118364
      vertex 18.781965 -2.175570 16.081966
    endloop
  endfacet
  facet normal -0.829494 -0.558515 0.000000
    outer loop
      vertex 18.781965 -2.175570 12.118034
      vertex 18.781965 -2.175570 16.081966
      vertex 18.702162 -2.057048 16.002163
    endloop
  endfacet
  facet normal -0.824012 -0.566573 0.000359
    outer loop
      vertex 18.722658 -2.089278 12.177341
      vertex 18.781965 -2.175570 12.118034
      vertex 18.702162 -2.057048 16.002163
    endloop
  endfacet
  facet normal -0.852691 -0.522416 -0.000167
    outer loop
      vertex 18.722658 -2.089278 12.177341
      vertex 18.702162 -2.057048 16.002163
      vertex 18.667950 -2.000000 12.232051
    endloop
  endfacet
  facet normal -0.857604 -0.514311 0.000000
    outer loop
      vertex 18.667950 -2.000000 12.232051
      vertex 18.702162 -2.057048 16.002163
      vertex 18.667950 -2.000000 15.967948
    endloop
  endfacet
  facet normal -0.882553 -0.470213 0.000000
    outer loop
      vertex 18.667950 -2.000000 12.232051
      vertex 18.667950 -2.000000 15.967948
      vertex 18.603889 -1.879764 15.903889
    endloop
  endfacet
  facet normal -0.878754 -0.477275 0.000298
    outer loop
      vertex 18.617989 -1.907981 12.282013
      vertex 18.667950 -2.000000 12.232051
      vertex 18.603889 -1.879764 15.903889
    endloop
  endfacet
  facet normal -0.902613 -0.430452 -0.000160
    outer loop
      vertex 18.617989 -1.907981 12.282013
      vertex 18.603889 -1.879764 15.903889
      vertex 18.572910 -1.813473 12.327091
    endloop
  endfacet
  facet normal -0.905955 -0.423373 0.000000
    outer loop
      vertex 18.572910 -1.813473 12.327091
      vertex 18.603889 -1.879764 15.903889
      vertex 18.572910 -1.813473 15.872909
    endloop
  endfacet
  facet normal -0.926237 -0.376941 0.000000
    outer loop
      vertex 18.572910 -1.813473 12.327091
      vertex 18.572910 -1.813473 15.872909
      vertex 18.524063 -1.693444 15.824064
    endloop
  endfacet
  facet normal -0.923840 -0.382778 0.000234
    outer loop
      vertex 18.532839 -1.716736 12.367161
      vertex 18.572910 -1.813473 12.327091
      vertex 18.524063 -1.693444 15.824064
    endloop
  endfacet
  facet normal -0.942658 -0.333762 -0.000144
    outer loop
      vertex 18.532839 -1.716736 12.367161
      vertex 18.524063 -1.693444 15.824064
      vertex 18.497887 -1.618034 12.402113
    endloop
  endfacet
  facet normal -0.960106 -0.279636 0.000000
    outer loop
      vertex 18.463509 -1.500000 15.500000
      vertex 18.497887 -1.618034 15.797887
      vertex 18.463509 -1.500000 15.763508
    endloop
  endfacet
  facet normal -0.973423 -0.229014 0.000000
    outer loop
      vertex 18.443705 -1.415823 12.456295
      vertex 18.463509 -1.500000 15.500000
      vertex 18.443705 -1.415823 15.500000
    endloop
  endfacet
  facet normal -0.944702 -0.327929 0.000000
    outer loop
      vertex 18.497887 -1.618034 12.402113
      vertex 18.524063 -1.693444 15.824064
      vertex 18.497887 -1.618034 15.797887
    endloop
  endfacet
  facet normal -0.960106 -0.279636 0.000000
    outer loop
      vertex 18.497887 -1.618034 12.402113
      vertex 18.497887 -1.618034 15.797887
      vertex 18.463509 -1.500000 15.500000
    endloop
  endfacet
  facet normal -0.958808 -0.284055 0.000183
    outer loop
      vertex 18.468149 -1.517638 12.431851
      vertex 18.497887 -1.618034 12.402113
      vertex 18.463509 -1.500000 15.500000
    endloop
  endfacet
  facet normal -0.972375 -0.233425 -0.000129
    outer loop
      vertex 18.468149 -1.517638 12.431851
      vertex 18.463509 -1.500000 15.500000
      vertex 18.443705 -1.415823 12.456295
    endloop
  endfacet
  facet normal -0.998629 -0.052343 0.000000
    outer loop
      vertex 18.400000 -1.000000 12.500000
      vertex 18.410957 -1.209057 15.500000
      vertex 18.400000 -1.000000 15.500000
    endloop
  endfacet
  facet normal -0.999654 -0.026224 0.001824
    outer loop
      vertex 18.410957 -1.209057 15.500000
      vertex 18.400000 -1.000000 12.500000
      vertex 18.402740 -1.104672 12.497259
    endloop
  endfacet
  facet normal -0.996916 -0.078474 -0.000000
    outer loop
      vertex 18.410957 -1.209057 15.500000
      vertex 18.402740 -1.104672 12.497259
      vertex 18.410957 -1.209057 12.489044
    endloop
  endfacet
  facet normal -0.987689 -0.156428 0.000000
    outer loop
      vertex 18.443705 -1.415823 15.500000
      vertex 18.410957 -1.209057 15.500000
      vertex 18.410957 -1.209057 12.489044
    endloop
  endfacet
  facet normal -0.991414 -0.130750 0.001804
    outer loop
      vertex 18.443705 -1.415823 15.500000
      vertex 18.410957 -1.209057 12.489044
      vertex 18.424623 -1.312869 12.475377
    endloop
  endfacet
  facet normal -0.983256 -0.182232 0.000000
    outer loop
      vertex 18.443705 -1.415823 12.456295
      vertex 18.443705 -1.415823 15.500000
      vertex 18.424623 -1.312869 12.475377
    endloop
  endfacet
  facet normal -1.000000 0.000000 0.000000
    outer loop
      vertex 29.000000 2.000000 0.000000
      vertex 29.000000 2.000000 2.000000
      vertex 29.000000 69.000000 2.000000
    endloop
  endfacet
  facet normal -1.000000 0.000000 0.000000
    outer loop
      vertex 29.000000 2.000000 0.000000
      vertex 29.000000 69.000000 2.000000
      vertex 29.000000 69.000000 0.000000
    endloop
  endfacet
  facet normal -0.052334 0.998630 0.000000
    outer loop
      vertex -1.209057 73.989044 -10.500000
      vertex -1.000000 74.000000 23.000000
      vertex -1.000000 74.000000 -10.500000
    endloop
  endfacet
  facet normal -0.052334 0.998630 0.000000
    outer loop
      vertex -1.209057 73.989044 23.000000
      vertex -1.000000 74.000000 23.000000
      vertex -1.209057 73.989044 -10.500000
    endloop
  endfacet
  facet normal -0.156419 0.987691 0.000000
    outer loop
      vertex -1.209057 73.989044 23.000000
      vertex -1.209057 73.989044 -10.500000
      vertex -1.415823 73.956299 -10.500000
    endloop
  endfacet
  facet normal -0.156419 0.987691 0.000000
    outer loop
      vertex -1.415823 73.956299 23.000000
      vertex -1.209057 73.989044 23.000000
      vertex -1.415823 73.956299 -10.500000
    endloop
  endfacet
  facet normal -0.258827 0.965924 0.000000
    outer loop
      vertex -1.415823 73.956299 23.000000
      vertex -1.415823 73.956299 -10.500000
      vertex -1.618034 73.902115 -10.500000
    endloop
  endfacet
  facet normal -0.258827 0.965924 0.000000
    outer loop
      vertex -1.618034 73.902115 23.000000
      vertex -1.415823 73.956299 23.000000
      vertex -1.618034 73.902115 -10.500000
    endloop
  endfacet
  facet normal -0.358390 0.933572 0.000000
    outer loop
      vertex -1.618034 73.902115 23.000000
      vertex -1.618034 73.902115 -10.500000
      vertex -1.813473 73.827087 -10.500000
    endloop
  endfacet
  facet normal -0.358390 0.933572 0.000000
    outer loop
      vertex -1.813473 73.827087 23.000000
      vertex -1.618034 73.902115 23.000000
      vertex -1.813473 73.827087 -10.500000
    endloop
  endfacet
  facet normal -0.453988 0.891008 0.000000
    outer loop
      vertex -1.813473 73.827087 23.000000
      vertex -1.813473 73.827087 -10.500000
      vertex -2.000000 73.732048 -10.500000
    endloop
  endfacet
  facet normal -0.453988 0.891008 0.000000
    outer loop
      vertex -2.000000 73.732048 23.000000
      vertex -1.813473 73.827087 23.000000
      vertex -2.000000 73.732048 -10.500000
    endloop
  endfacet
  facet normal -0.544629 0.838677 0.000000
    outer loop
      vertex -2.000000 73.732048 23.000000
      vertex -2.000000 73.732048 -10.500000
      vertex -2.175570 73.618034 -10.500000
    endloop
  endfacet
  facet normal -0.544629 0.838677 0.000000
    outer loop
      vertex -2.175570 73.618034 23.000000
      vertex -2.000000 73.732048 23.000000
      vertex -2.175570 73.618034 -10.500000
    endloop
  endfacet
  facet normal -0.629321 0.777146 0.000000
    outer loop
      vertex -2.175570 73.618034 23.000000
      vertex -2.175570 73.618034 -10.500000
      vertex -2.338261 73.486290 -10.500000
    endloop
  endfacet
  facet normal -0.629321 0.777146 0.000000
    outer loop
      vertex -2.338261 73.486290 23.000000
      vertex -2.175570 73.618034 23.000000
      vertex -2.338261 73.486290 -10.500000
    endloop
  endfacet
  facet normal -0.707099 0.707114 0.000000
    outer loop
      vertex -2.338261 73.486290 23.000000
      vertex -2.338261 73.486290 -10.500000
      vertex -2.486290 73.338264 -10.500000
    endloop
  endfacet
  facet normal -0.707099 0.707114 0.000000
    outer loop
      vertex -2.486290 73.338264 23.000000
      vertex -2.338261 73.486290 23.000000
      vertex -2.486290 73.338264 -10.500000
    endloop
  endfacet
  facet normal -0.777144 0.629323 0.000000
    outer loop
      vertex -2.486290 73.338264 23.000000
      vertex -2.486290 73.338264 -10.500000
      vertex -2.618034 73.175575 -10.500000
    endloop
  endfacet
  facet normal -0.777144 0.629323 0.000000
    outer loop
      vertex -2.618034 73.175575 23.000000
      vertex -2.486290 73.338264 23.000000
      vertex -2.618034 73.175575 -10.500000
    endloop
  endfacet
  facet normal -0.838677 0.544629 0.000000
    outer loop
      vertex -2.618034 73.175575 23.000000
      vertex -2.618034 73.175575 -10.500000
      vertex -2.732051 73.000000 -10.500000
    endloop
  endfacet
  facet normal -0.838677 0.544629 0.000000
    outer loop
      vertex -2.732051 73.000000 23.000000
      vertex -2.618034 73.175575 23.000000
      vertex -2.732051 73.000000 -10.500000
    endloop
  endfacet
  facet normal -0.891003 0.453997 0.000000
    outer loop
      vertex -2.732051 73.000000 23.000000
      vertex -2.732051 73.000000 -10.500000
      vertex -2.827091 72.813477 -10.500000
    endloop
  endfacet
  facet normal -0.891003 0.453997 0.000000
    outer loop
      vertex -2.827091 72.813477 23.000000
      vertex -2.732051 73.000000 23.000000
      vertex -2.827091 72.813477 -10.500000
    endloop
  endfacet
  facet normal -0.933582 0.358364 0.000000
    outer loop
      vertex -2.827091 72.813477 23.000000
      vertex -2.827091 72.813477 -10.500000
      vertex -2.902113 72.618034 -10.500000
    endloop
  endfacet
  facet normal -0.933582 0.358364 0.000000
    outer loop
      vertex -2.902113 72.618034 23.000000
      vertex -2.827091 72.813477 23.000000
      vertex -2.902113 72.618034 -10.500000
    endloop
  endfacet
  facet normal -0.965926 0.258820 0.000000
    outer loop
      vertex -2.902113 72.618034 23.000000
      vertex -2.902113 72.618034 -10.500000
      vertex -2.956295 72.415825 -10.500000
    endloop
  endfacet
  facet normal -0.965926 0.258820 0.000000
    outer loop
      vertex -2.956295 72.415825 23.000000
      vertex -2.902113 72.618034 23.000000
      vertex -2.956295 72.415825 -10.500000
    endloop
  endfacet
  facet normal -0.987688 0.156436 0.000000
    outer loop
      vertex -2.956295 72.415825 23.000000
      vertex -2.956295 72.415825 -10.500000
      vertex -2.989044 72.209061 -10.500000
    endloop
  endfacet
  facet normal -0.987688 0.156436 0.000000
    outer loop
      vertex -2.989044 72.209061 23.000000
      vertex -2.956295 72.415825 23.000000
      vertex -2.989044 72.209061 -10.500000
    endloop
  endfacet
  facet normal -0.998630 0.052335 0.000000
    outer loop
      vertex -2.989044 72.209061 23.000000
      vertex -2.989044 72.209061 -10.500000
      vertex -3.000000 72.000000 -10.500000
    endloop
  endfacet
  facet normal -0.998630 0.052335 0.000000
    outer loop
      vertex -3.000000 72.000000 23.000000
      vertex -2.989044 72.209061 23.000000
      vertex -3.000000 72.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 -1.000000 -9.500000
      vertex 31.199999 -1.000000 -9.500000
      vertex 31.218704 -0.828024 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 -1.000000 -9.500000
      vertex 31.314514 -1.412443 -9.500000
      vertex 31.241877 -1.255441 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 -1.000000 -9.500000
      vertex 31.241877 -1.255441 -9.500000
      vertex 31.204689 -1.086495 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 31.199999 -1.000000 -9.500000
      vertex 32.000000 -1.000000 -9.500000
      vertex 31.204689 -1.086495 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 -1.000000 -9.500000
      vertex 31.703890 -1.743181 -9.500000
      vertex 31.551052 -1.662151 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 -1.000000 -9.500000
      vertex 31.551052 -1.662151 -9.500000
      vertex 31.419203 -1.550160 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 31.314514 -1.412443 -9.500000
      vertex 32.000000 -1.000000 -9.500000
      vertex 31.419203 -1.550160 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 -1.000000 -9.500000
      vertex 32.214024 -1.770840 -9.500000
      vertex 32.043312 -1.798827 -9.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 32.000000 -1.000000 -9.500000
      vertex 32.043312 -1.798827 -9.500000
      vertex 31.870573 -1.789461 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 31.703890 -1.743181 -9.500000
      vertex 32.000000 -1.000000 -9.500000
      vertex 31.870573 -1.789461 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 -1.000000 -9.500000
      vertex 32.517910 -1.609730 -9.500000
      vertex 32.448952 -1.662151 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 -1.000000 -9.500000
      vertex 32.448952 -1.662151 -9.500000
      vertex 32.374729 -1.706810 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.214024 -1.770840 -9.500000
      vertex 32.000000 -1.000000 -9.500000
      vertex 32.374729 -1.706810 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 -1.000000 -9.500000
      vertex 32.781296 -1.171976 -9.500000
      vertex 32.726059 -1.335911 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 -1.000000 -9.500000
      vertex 32.726059 -1.335911 -9.500000
      vertex 32.636875 -1.484139 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.517910 -1.609730 -9.500000
      vertex 32.000000 -1.000000 -9.500000
      vertex 32.636875 -1.484139 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 -1.000000 -9.500000
      vertex 32.726059 -0.664089 -9.500000
      vertex 32.781296 -0.828024 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 -1.000000 -9.500000
      vertex 32.781296 -0.828024 -9.500000
      vertex 32.799999 -1.000000 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.781296 -1.171976 -9.500000
      vertex 32.000000 -1.000000 -9.500000
      vertex 32.799999 -1.000000 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 -1.000000 -9.500000
      vertex 32.448952 -0.337849 -9.500000
      vertex 32.517910 -0.390270 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 -1.000000 -9.500000
      vertex 32.517910 -0.390270 -9.500000
      vertex 32.636875 -0.515861 -9.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 32.726059 -0.664089 -9.500000
      vertex 32.000000 -1.000000 -9.500000
      vertex 32.636875 -0.515861 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 -1.000000 -9.500000
      vertex 31.956688 -0.201173 -9.500000
      vertex 32.129425 -0.210539 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 -1.000000 -9.500000
      vertex 32.129425 -0.210539 -9.500000
      vertex 32.296108 -0.256819 -9.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 32.448952 -0.337849 -9.500000
      vertex 32.000000 -1.000000 -9.500000
      vertex 32.296108 -0.256819 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 -1.000000 -9.500000
      vertex 31.482090 -0.390270 -9.500000
      vertex 31.625275 -0.293190 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 -1.000000 -9.500000
      vertex 31.625275 -0.293190 -9.500000
      vertex 31.785976 -0.229160 -9.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 31.956688 -0.201173 -9.500000
      vertex 32.000000 -1.000000 -9.500000
      vertex 31.785976 -0.229160 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 -1.000000 -9.500000
      vertex 31.218704 -0.828024 -9.500000
      vertex 31.273939 -0.664089 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 -1.000000 -9.500000
      vertex 31.273939 -0.664089 -9.500000
      vertex 31.363127 -0.515861 -9.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 31.482090 -0.390270 -9.500000
      vertex 32.000000 -1.000000 -9.500000
      vertex 31.363127 -0.515861 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 9.900000 -1.000000 12.500000
      vertex 18.400000 -1.000000 12.500000
      vertex 18.400000 -0.000000 12.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 9.900000 -1.000000 12.500000
      vertex 18.400000 -0.000000 12.500000
      vertex 9.900000 -0.000000 12.500000
    endloop
  endfacet
  facet normal 0.994138 -0.108121 0.000000
    outer loop
      vertex -1.976621 72.614967 -9.500000
      vertex -2.000000 72.400002 -9.500000
      vertex -2.000000 72.400002 -10.500000
    endloop
  endfacet
  facet normal 0.994138 -0.108121 0.000000
    outer loop
      vertex -1.976621 72.614967 -9.500000
      vertex -2.000000 72.400002 -10.500000
      vertex -1.976621 72.614967 -10.500000
    endloop
  endfacet
  facet normal 0.947653 -0.319303 0.000000
    outer loop
      vertex -1.907575 72.819885 -9.500000
      vertex -1.976621 72.614967 -9.500000
      vertex -1.976621 72.614967 -10.500000
    endloop
  endfacet
  facet normal 0.947653 -0.319303 0.000000
    outer loop
      vertex -1.907575 72.819885 -9.500000
      vertex -1.976621 72.614967 -10.500000
      vertex -1.907575 72.819885 -10.500000
    endloop
  endfacet
  facet normal 0.856870 -0.515533 0.000000
    outer loop
      vertex -1.796093 73.005180 -9.500000
      vertex -1.907575 72.819885 -9.500000
      vertex -1.907575 72.819885 -10.500000
    endloop
  endfacet
  facet normal 0.856870 -0.515533 0.000000
    outer loop
      vertex -1.796093 73.005180 -9.500000
      vertex -1.907575 72.819885 -10.500000
      vertex -1.796093 73.005180 -10.500000
    endloop
  endfacet
  facet normal 0.725983 -0.687712 0.000000
    outer loop
      vertex -1.647386 73.162163 -9.500000
      vertex -1.796093 73.005180 -9.500000
      vertex -1.796093 73.005180 -10.500000
    endloop
  endfacet
  facet normal 0.725983 -0.687712 0.000000
    outer loop
      vertex -1.647386 73.162163 -9.500000
      vertex -1.796093 73.005180 -10.500000
      vertex -1.647386 73.162163 -10.500000
    endloop
  endfacet
  facet normal 0.561173 -0.827699 0.000000
    outer loop
      vertex -1.468408 73.283508 -9.500000
      vertex -1.647386 73.162163 -9.500000
      vertex -1.647386 73.162163 -10.500000
    endloop
  endfacet
  facet normal 0.561173 -0.827699 0.000000
    outer loop
      vertex -1.468408 73.283508 -9.500000
      vertex -1.647386 73.162163 -10.500000
      vertex -1.468408 73.283508 -10.500000
    endloop
  endfacet
  facet normal 0.370147 -0.928973 0.000000
    outer loop
      vertex -1.267528 73.363548 -9.500000
      vertex -1.468408 73.283508 -9.500000
      vertex -1.468408 73.283508 -10.500000
    endloop
  endfacet
  facet normal 0.370147 -0.928973 0.000000
    outer loop
      vertex -1.267528 73.363548 -9.500000
      vertex -1.468408 73.283508 -10.500000
      vertex -1.267528 73.363548 -10.500000
    endloop
  endfacet
  facet normal 0.161770 -0.986829 0.000000
    outer loop
      vertex -1.054139 73.398529 -9.500000
      vertex -1.267528 73.363548 -9.500000
      vertex -1.267528 73.363548 -10.500000
    endloop
  endfacet
  facet normal 0.161770 -0.986829 0.000000
    outer loop
      vertex -1.054139 73.398529 -9.500000
      vertex -1.267528 73.363548 -10.500000
      vertex -1.054139 73.398529 -10.500000
    endloop
  endfacet
  facet normal -0.054123 -0.998534 0.000000
    outer loop
      vertex -0.838218 73.386826 -9.500000
      vertex -1.054139 73.398529 -9.500000
      vertex -1.054139 73.398529 -10.500000
    endloop
  endfacet
  facet normal -0.054123 -0.998534 -0.000000
    outer loop
      vertex -0.838218 73.386826 -9.500000
      vertex -1.054139 73.398529 -10.500000
      vertex -0.838218 73.386826 -10.500000
    endloop
  endfacet
  facet normal -0.267512 -0.963554 0.000000
    outer loop
      vertex -0.629862 73.328979 -9.500000
      vertex -0.838218 73.386826 -9.500000
      vertex -0.838218 73.386826 -10.500000
    endloop
  endfacet
  facet normal -0.267512 -0.963554 -0.000000
    outer loop
      vertex -0.629862 73.328979 -9.500000
      vertex -0.838218 73.386826 -10.500000
      vertex -0.629862 73.328979 -10.500000
    endloop
  endfacet
  facet normal -0.468409 -0.883512 0.000000
    outer loop
      vertex -0.438813 73.227692 -9.500000
      vertex -0.629862 73.328979 -9.500000
      vertex -0.629862 73.328979 -10.500000
    endloop
  endfacet
  facet normal -0.468409 -0.883512 -0.000000
    outer loop
      vertex -0.438813 73.227692 -9.500000
      vertex -0.629862 73.328979 -10.500000
      vertex -0.438813 73.227692 -10.500000
    endloop
  endfacet
  facet normal -0.605185 -0.796084 0.000000
    outer loop
      vertex -0.352614 73.162163 -9.500000
      vertex -0.438813 73.227692 -9.500000
      vertex -0.438813 73.227692 -10.500000
    endloop
  endfacet
  facet normal -0.605185 -0.796084 -0.000000
    outer loop
      vertex -0.352614 73.162163 -9.500000
      vertex -0.438813 73.227692 -10.500000
      vertex -0.352614 73.162163 -10.500000
    endloop
  endfacet
  facet normal -0.725984 -0.687712 0.000000
    outer loop
      vertex -0.203907 73.005180 -9.500000
      vertex -0.352614 73.162163 -9.500000
      vertex -0.352614 73.162163 -10.500000
    endloop
  endfacet
  facet normal -0.725984 -0.687712 -0.000000
    outer loop
      vertex -0.203907 73.005180 -9.500000
      vertex -0.352614 73.162163 -10.500000
      vertex -0.203907 73.005180 -10.500000
    endloop
  endfacet
  facet normal -0.856869 -0.515533 0.000000
    outer loop
      vertex -0.092425 72.819885 -9.500000
      vertex -0.203907 73.005180 -9.500000
      vertex -0.203907 73.005180 -10.500000
    endloop
  endfacet
  facet normal -0.856869 -0.515533 -0.000000
    outer loop
      vertex -0.092425 72.819885 -9.500000
      vertex -0.203907 73.005180 -10.500000
      vertex -0.092425 72.819885 -10.500000
    endloop
  endfacet
  facet normal -0.947653 -0.319303 0.000000
    outer loop
      vertex -0.023379 72.614967 -9.500000
      vertex -0.092425 72.819885 -9.500000
      vertex -0.092425 72.819885 -10.500000
    endloop
  endfacet
  facet normal -0.947653 -0.319303 -0.000000
    outer loop
      vertex -0.023379 72.614967 -9.500000
      vertex -0.092425 72.819885 -10.500000
      vertex -0.023379 72.614967 -10.500000
    endloop
  endfacet
  facet normal -0.994138 -0.108121 0.000000
    outer loop
      vertex -0.000000 72.400002 -9.500000
      vertex -0.023379 72.614967 -9.500000
      vertex -0.023379 72.614967 -10.500000
    endloop
  endfacet
  facet normal -0.994138 -0.108121 -0.000000
    outer loop
      vertex -0.000000 72.400002 -9.500000
      vertex -0.023379 72.614967 -10.500000
      vertex -0.000000 72.400002 -10.500000
    endloop
  endfacet
  facet normal -0.994138 0.108121 0.000000
    outer loop
      vertex -0.023379 72.185036 -9.500000
      vertex -0.000000 72.400002 -9.500000
      vertex -0.000000 72.400002 -10.500000
    endloop
  endfacet
  facet normal -0.994138 0.108121 0.000000
    outer loop
      vertex -0.023379 72.185036 -9.500000
      vertex -0.000000 72.400002 -10.500000
      vertex -0.023379 72.185036 -10.500000
    endloop
  endfacet
  facet normal -0.947656 0.319292 0.000000
    outer loop
      vertex -0.092425 71.980110 -9.500000
      vertex -0.023379 72.185036 -9.500000
      vertex -0.023379 72.185036 -10.500000
    endloop
  endfacet
  facet normal -0.947656 0.319292 0.000000
    outer loop
      vertex -0.092425 71.980110 -9.500000
      vertex -0.023379 72.185036 -10.500000
      vertex -0.092425 71.980110 -10.500000
    endloop
  endfacet
  facet normal -0.856860 0.515549 0.000000
    outer loop
      vertex -0.203907 71.794823 -9.500000
      vertex -0.092425 71.980110 -9.500000
      vertex -0.092425 71.980110 -10.500000
    endloop
  endfacet
  facet normal -0.856860 0.515549 0.000000
    outer loop
      vertex -0.203907 71.794823 -9.500000
      vertex -0.092425 71.980110 -10.500000
      vertex -0.203907 71.794823 -10.500000
    endloop
  endfacet
  facet normal -0.725984 0.687712 0.000000
    outer loop
      vertex -0.352614 71.637840 -9.500000
      vertex -0.203907 71.794823 -9.500000
      vertex -0.203907 71.794823 -10.500000
    endloop
  endfacet
  facet normal -0.725984 0.687712 0.000000
    outer loop
      vertex -0.352614 71.637840 -9.500000
      vertex -0.203907 71.794823 -10.500000
      vertex -0.352614 71.637840 -10.500000
    endloop
  endfacet
  facet normal -0.605185 0.796084 0.000000
    outer loop
      vertex -0.438813 71.572311 -9.500000
      vertex -0.352614 71.637840 -9.500000
      vertex -0.352614 71.637840 -10.500000
    endloop
  endfacet
  facet normal -0.605185 0.796084 0.000000
    outer loop
      vertex -0.438813 71.572311 -9.500000
      vertex -0.352614 71.637840 -10.500000
      vertex -0.438813 71.572311 -10.500000
    endloop
  endfacet
  facet normal -0.515511 0.856883 0.000000
    outer loop
      vertex -0.531592 71.516495 -9.500000
      vertex -0.438813 71.572311 -9.500000
      vertex -0.438813 71.572311 -10.500000
    endloop
  endfacet
  facet normal -0.515511 0.856883 0.000000
    outer loop
      vertex -0.531592 71.516495 -9.500000
      vertex -0.438813 71.572311 -10.500000
      vertex -0.531592 71.516495 -10.500000
    endloop
  endfacet
  facet normal -0.370177 0.928961 0.000000
    outer loop
      vertex -0.732472 71.436447 -9.500000
      vertex -0.531592 71.516495 -9.500000
      vertex -0.531592 71.516495 -10.500000
    endloop
  endfacet
  facet normal -0.370177 0.928961 0.000000
    outer loop
      vertex -0.732472 71.436447 -9.500000
      vertex -0.531592 71.516495 -10.500000
      vertex -0.732472 71.436447 -10.500000
    endloop
  endfacet
  facet normal -0.161770 0.986829 0.000000
    outer loop
      vertex -0.945861 71.401466 -9.500000
      vertex -0.732472 71.436447 -9.500000
      vertex -0.732472 71.436447 -10.500000
    endloop
  endfacet
  facet normal -0.161770 0.986829 0.000000
    outer loop
      vertex -0.945861 71.401466 -9.500000
      vertex -0.732472 71.436447 -10.500000
      vertex -0.945861 71.401466 -10.500000
    endloop
  endfacet
  facet normal 0.054158 0.998532 0.000000
    outer loop
      vertex -1.161782 71.413177 -9.500000
      vertex -0.945861 71.401466 -9.500000
      vertex -0.945861 71.401466 -10.500000
    endloop
  endfacet
  facet normal 0.054158 0.998532 0.000000
    outer loop
      vertex -1.161782 71.413177 -9.500000
      vertex -0.945861 71.401466 -10.500000
      vertex -1.161782 71.413177 -10.500000
    endloop
  endfacet
  facet normal 0.267512 0.963554 0.000000
    outer loop
      vertex -1.370138 71.471024 -9.500000
      vertex -1.161782 71.413177 -9.500000
      vertex -1.161782 71.413177 -10.500000
    endloop
  endfacet
  facet normal 0.267512 0.963554 0.000000
    outer loop
      vertex -1.370138 71.471024 -9.500000
      vertex -1.161782 71.413177 -10.500000
      vertex -1.370138 71.471024 -10.500000
    endloop
  endfacet
  facet normal 0.468409 0.883512 0.000000
    outer loop
      vertex -1.561187 71.572311 -9.500000
      vertex -1.370138 71.471024 -9.500000
      vertex -1.370138 71.471024 -10.500000
    endloop
  endfacet
  facet normal 0.468409 0.883512 0.000000
    outer loop
      vertex -1.561187 71.572311 -9.500000
      vertex -1.370138 71.471024 -10.500000
      vertex -1.561187 71.572311 -10.500000
    endloop
  endfacet
  facet normal 0.647393 0.762157 0.000000
    outer loop
      vertex -1.725995 71.712303 -9.500000
      vertex -1.561187 71.572311 -9.500000
      vertex -1.561187 71.572311 -10.500000
    endloop
  endfacet
  facet normal 0.647393 0.762157 0.000000
    outer loop
      vertex -1.725995 71.712303 -9.500000
      vertex -1.561187 71.572311 -10.500000
      vertex -1.725995 71.712303 -10.500000
    endloop
  endfacet
  facet normal 0.796087 0.605182 0.000000
    outer loop
      vertex -1.856857 71.884445 -9.500000
      vertex -1.725995 71.712303 -9.500000
      vertex -1.725995 71.712303 -10.500000
    endloop
  endfacet
  facet normal 0.796087 0.605182 0.000000
    outer loop
      vertex -1.856857 71.884445 -9.500000
      vertex -1.725995 71.712303 -10.500000
      vertex -1.856857 71.884445 -10.500000
    endloop
  endfacet
  facet normal 0.907581 0.419878 0.000000
    outer loop
      vertex -1.947653 72.080704 -9.500000
      vertex -1.856857 71.884445 -9.500000
      vertex -1.856857 71.884445 -10.500000
    endloop
  endfacet
  facet normal 0.907581 0.419878 0.000000
    outer loop
      vertex -1.947653 72.080704 -9.500000
      vertex -1.856857 71.884445 -10.500000
      vertex -1.947653 72.080704 -10.500000
    endloop
  endfacet
  facet normal 0.976619 0.214978 0.000000
    outer loop
      vertex -1.994138 72.291878 -9.500000
      vertex -1.947653 72.080704 -9.500000
      vertex -1.947653 72.080704 -10.500000
    endloop
  endfacet
  facet normal 0.976619 0.214978 0.000000
    outer loop
      vertex -1.994138 72.291878 -9.500000
      vertex -1.947653 72.080704 -10.500000
      vertex -1.994138 72.291878 -10.500000
    endloop
  endfacet
  facet normal 0.998534 0.054137 0.000000
    outer loop
      vertex -2.000000 72.400002 -9.500000
      vertex -1.994138 72.291878 -9.500000
      vertex -1.994138 72.291878 -10.500000
    endloop
  endfacet
  facet normal 0.998534 0.054137 0.000000
    outer loop
      vertex -2.000000 72.400002 -9.500000
      vertex -1.994138 72.291878 -10.500000
      vertex -2.000000 72.400002 -10.500000
    endloop
  endfacet
  facet normal -1.000000 0.000000 0.000000
    outer loop
      vertex -3.000000 -1.000000 23.000000
      vertex -3.000000 6.500000 14.500000
      vertex -3.000000 -1.000000 -10.500000
    endloop
  endfacet
  facet normal -1.000000 0.000000 0.000000
    outer loop
      vertex -3.000000 72.000000 -10.500000
      vertex -3.000000 71.099998 23.000000
      vertex -3.000000 72.000000 23.000000
    endloop
  endfacet
  facet normal -1.000000 0.000000 0.000000
    outer loop
      vertex -3.000000 71.199997 -10.500000
      vertex -3.000000 -1.000000 -10.500000
      vertex -3.000000 6.500000 14.500000
    endloop
  endfacet
  facet normal -1.000000 0.000000 0.000000
    outer loop
      vertex -3.000000 71.199997 -10.500000
      vertex -3.000000 6.500000 14.500000
      vertex -3.000000 15.500000 14.500000
    endloop
  endfacet
  facet normal -1.000000 0.000000 0.000000
    outer loop
      vertex -3.000000 15.500000 22.000000
      vertex -3.000000 71.199997 -10.500000
      vertex -3.000000 15.500000 14.500000
    endloop
  endfacet
  facet normal -1.000000 0.000000 0.000000
    outer loop
      vertex -3.000000 71.099998 23.000000
      vertex -3.000000 72.000000 -10.500000
      vertex -3.000000 71.199997 -10.500000
    endloop
  endfacet
  facet normal -1.000000 0.000000 -0.000000
    outer loop
      vertex -3.000000 71.099998 23.000000
      vertex -3.000000 71.199997 -10.500000
      vertex -3.000000 15.500000 22.000000
    endloop
  endfacet
  facet normal -1.000000 0.000000 0.000000
    outer loop
      vertex -3.000000 -1.000000 23.000000
      vertex -3.000000 71.099998 23.000000
      vertex -3.000000 15.500000 22.000000
    endloop
  endfacet
  facet normal -1.000000 0.000000 0.000000
    outer loop
      vertex -3.000000 -1.000000 23.000000
      vertex -3.000000 15.500000 22.000000
      vertex -3.000000 6.500000 22.000000
    endloop
  endfacet
  facet normal -1.000000 0.000000 0.000000
    outer loop
      vertex -3.000000 6.500000 14.500000
      vertex -3.000000 -1.000000 23.000000
      vertex -3.000000 6.500000 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 72.400002 -9.500000
      vertex -2.000000 72.400002 -9.500000
      vertex -1.976621 72.614967 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 72.400002 -9.500000
      vertex -1.856857 71.884445 -9.500000
      vertex -1.947653 72.080704 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 72.400002 -9.500000
      vertex -1.947653 72.080704 -9.500000
      vertex -1.994138 72.291878 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -2.000000 72.400002 -9.500000
      vertex -1.000000 72.400002 -9.500000
      vertex -1.994138 72.291878 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 72.400002 -9.500000
      vertex -1.370138 71.471024 -9.500000
      vertex -1.561187 71.572311 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 72.400002 -9.500000
      vertex -1.561187 71.572311 -9.500000
      vertex -1.725995 71.712303 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.856857 71.884445 -9.500000
      vertex -1.000000 72.400002 -9.500000
      vertex -1.725995 71.712303 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 72.400002 -9.500000
      vertex -0.732472 71.436447 -9.500000
      vertex -0.945861 71.401466 -9.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex -1.000000 72.400002 -9.500000
      vertex -0.945861 71.401466 -9.500000
      vertex -1.161782 71.413177 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.370138 71.471024 -9.500000
      vertex -1.000000 72.400002 -9.500000
      vertex -1.161782 71.413177 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 72.400002 -9.500000
      vertex -0.352614 71.637840 -9.500000
      vertex -0.438813 71.572311 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 72.400002 -9.500000
      vertex -0.438813 71.572311 -9.500000
      vertex -0.531592 71.516495 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.732472 71.436447 -9.500000
      vertex -1.000000 72.400002 -9.500000
      vertex -0.531592 71.516495 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 72.400002 -9.500000
      vertex -0.023379 72.185036 -9.500000
      vertex -0.092425 71.980110 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 72.400002 -9.500000
      vertex -0.092425 71.980110 -9.500000
      vertex -0.203907 71.794823 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.352614 71.637840 -9.500000
      vertex -1.000000 72.400002 -9.500000
      vertex -0.203907 71.794823 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 72.400002 -9.500000
      vertex -0.092425 72.819885 -9.500000
      vertex -0.023379 72.614967 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 72.400002 -9.500000
      vertex -0.023379 72.614967 -9.500000
      vertex -0.000000 72.400002 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.023379 72.185036 -9.500000
      vertex -1.000000 72.400002 -9.500000
      vertex -0.000000 72.400002 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 72.400002 -9.500000
      vertex -0.438813 73.227692 -9.500000
      vertex -0.352614 73.162163 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 72.400002 -9.500000
      vertex -0.352614 73.162163 -9.500000
      vertex -0.203907 73.005180 -9.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex -0.092425 72.819885 -9.500000
      vertex -1.000000 72.400002 -9.500000
      vertex -0.203907 73.005180 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 72.400002 -9.500000
      vertex -1.054139 73.398529 -9.500000
      vertex -0.838218 73.386826 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 72.400002 -9.500000
      vertex -0.838218 73.386826 -9.500000
      vertex -0.629862 73.328979 -9.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex -0.438813 73.227692 -9.500000
      vertex -1.000000 72.400002 -9.500000
      vertex -0.629862 73.328979 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 72.400002 -9.500000
      vertex -1.647386 73.162163 -9.500000
      vertex -1.468408 73.283508 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 72.400002 -9.500000
      vertex -1.468408 73.283508 -9.500000
      vertex -1.267528 73.363548 -9.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex -1.054139 73.398529 -9.500000
      vertex -1.000000 72.400002 -9.500000
      vertex -1.267528 73.363548 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 72.400002 -9.500000
      vertex -1.976621 72.614967 -9.500000
      vertex -1.907575 72.819885 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 72.400002 -9.500000
      vertex -1.907575 72.819885 -9.500000
      vertex -1.796093 73.005180 -9.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex -1.647386 73.162163 -9.500000
      vertex -1.000000 72.400002 -9.500000
      vertex -1.796093 73.005180 -9.500000
    endloop
  endfacet
  facet normal 1.000000 0.000000 0.000000
    outer loop
      vertex 0.000000 0.000000 -10.500000
      vertex 0.000000 39.500000 0.000000
      vertex 0.000000 0.000000 0.000000
    endloop
  endfacet
  facet normal 1.000000 0.000000 0.000000
    outer loop
      vertex 0.000000 0.000000 2.000000
      vertex 0.000000 14.000000 16.000000
      vertex 0.000000 8.000000 16.000000
    endloop
  endfacet
  facet normal 1.000000 -0.000000 0.000000
    outer loop
      vertex -0.000000 62.299999 0.000000
      vertex -0.000000 71.000000 -10.500000
      vertex -0.000000 71.000000 0.000000
    endloop
  endfacet
  facet normal 1.000000 0.000000 0.000000
    outer loop
      vertex 0.000000 0.000000 23.000000
      vertex 0.000000 14.000000 20.500000
      vertex -0.000000 71.000000 23.000000
    endloop
  endfacet
  facet normal 1.000000 0.000000 -0.000000
    outer loop
      vertex 0.000000 39.500000 0.000000
      vertex 0.000000 0.000000 -10.500000
      vertex -0.000000 71.000000 -10.500000
    endloop
  endfacet
  facet normal 1.000000 0.000000 0.000000
    outer loop
      vertex 0.000000 39.500000 0.000000
      vertex -0.000000 71.000000 -10.500000
      vertex -0.000000 62.299999 0.000000
    endloop
  endfacet
  facet normal 1.000000 0.000000 0.000000
    outer loop
      vertex 0.000000 39.500000 2.000000
      vertex 0.000000 39.500000 0.000000
      vertex -0.000000 62.299999 0.000000
    endloop
  endfacet
  facet normal 1.000000 0.000000 -0.000000
    outer loop
      vertex 0.000000 39.500000 2.000000
      vertex -0.000000 62.299999 0.000000
      vertex 0.000000 62.299999 2.000000
    endloop
  endfacet
  facet normal 1.000000 0.000000 0.000000
    outer loop
      vertex 0.000000 0.000000 23.000000
      vertex 0.000000 0.000000 2.000000
      vertex 0.000000 8.000000 16.000000
    endloop
  endfacet
  facet normal 1.000000 0.000000 0.000000
    outer loop
      vertex 0.000000 0.000000 23.000000
      vertex 0.000000 8.000000 16.000000
      vertex 0.000000 8.000000 20.500000
    endloop
  endfacet
  facet normal 1.000000 0.000000 0.000000
    outer loop
      vertex 0.000000 14.000000 20.500000
      vertex 0.000000 0.000000 23.000000
      vertex 0.000000 8.000000 20.500000
    endloop
  endfacet
  facet normal 1.000000 0.000000 0.000000
    outer loop
      vertex 0.000000 14.000000 16.000000
      vertex 0.000000 0.000000 2.000000
      vertex 0.000000 39.500000 2.000000
    endloop
  endfacet
  facet normal 1.000000 0.000000 0.000000
    outer loop
      vertex 0.000000 14.000000 16.000000
      vertex 0.000000 39.500000 2.000000
      vertex 0.000000 62.299999 2.000000
    endloop
  endfacet
  facet normal 1.000000 0.000000 0.000000
    outer loop
      vertex 0.000000 14.000000 20.500000
      vertex 0.000000 14.000000 16.000000
      vertex 0.000000 62.299999 2.000000
    endloop
  endfacet
  facet normal 1.000000 0.000000 0.000000
    outer loop
      vertex 0.000000 14.000000 20.500000
      vertex 0.000000 62.299999 2.000000
      vertex -0.000000 71.000000 2.000000
    endloop
  endfacet
  facet normal 1.000000 0.000000 0.000000
    outer loop
      vertex -0.000000 71.000000 23.000000
      vertex 0.000000 14.000000 20.500000
      vertex -0.000000 71.000000 2.000000
    endloop
  endfacet
  facet normal 0.994137 -0.108125 0.000000
    outer loop
      vertex 31.023380 72.614967 -9.500000
      vertex 31.000000 72.400002 -9.500000
      vertex 31.000000 72.400002 -10.500000
    endloop
  endfacet
  facet normal 0.994137 -0.108125 0.000000
    outer loop
      vertex 31.023380 72.614967 -9.500000
      vertex 31.000000 72.400002 -10.500000
      vertex 31.023380 72.614967 -10.500000
    endloop
  endfacet
  facet normal 0.947654 -0.319298 0.000000
    outer loop
      vertex 31.092424 72.819885 -9.500000
      vertex 31.023380 72.614967 -9.500000
      vertex 31.023380 72.614967 -10.500000
    endloop
  endfacet
  facet normal 0.947654 -0.319298 0.000000
    outer loop
      vertex 31.092424 72.819885 -9.500000
      vertex 31.023380 72.614967 -10.500000
      vertex 31.092424 72.819885 -10.500000
    endloop
  endfacet
  facet normal 0.856869 -0.515534 0.000000
    outer loop
      vertex 31.203907 73.005180 -9.500000
      vertex 31.092424 72.819885 -9.500000
      vertex 31.092424 72.819885 -10.500000
    endloop
  endfacet
  facet normal 0.856869 -0.515534 0.000000
    outer loop
      vertex 31.203907 73.005180 -9.500000
      vertex 31.092424 72.819885 -10.500000
      vertex 31.203907 73.005180 -10.500000
    endloop
  endfacet
  facet normal 0.725984 -0.687711 0.000000
    outer loop
      vertex 31.352613 73.162163 -9.500000
      vertex 31.203907 73.005180 -9.500000
      vertex 31.203907 73.005180 -10.500000
    endloop
  endfacet
  facet normal 0.725984 -0.687711 0.000000
    outer loop
      vertex 31.352613 73.162163 -9.500000
      vertex 31.203907 73.005180 -10.500000
      vertex 31.352613 73.162163 -10.500000
    endloop
  endfacet
  facet normal 0.561173 -0.827699 0.000000
    outer loop
      vertex 31.531591 73.283508 -9.500000
      vertex 31.352613 73.162163 -9.500000
      vertex 31.352613 73.162163 -10.500000
    endloop
  endfacet
  facet normal 0.561173 -0.827699 0.000000
    outer loop
      vertex 31.531591 73.283508 -9.500000
      vertex 31.352613 73.162163 -10.500000
      vertex 31.531591 73.283508 -10.500000
    endloop
  endfacet
  facet normal 0.370143 -0.928975 0.000000
    outer loop
      vertex 31.732473 73.363548 -9.500000
      vertex 31.531591 73.283508 -9.500000
      vertex 31.531591 73.283508 -10.500000
    endloop
  endfacet
  facet normal 0.370143 -0.928975 0.000000
    outer loop
      vertex 31.732473 73.363548 -9.500000
      vertex 31.531591 73.283508 -10.500000
      vertex 31.732473 73.363548 -10.500000
    endloop
  endfacet
  facet normal 0.161771 -0.986828 0.000000
    outer loop
      vertex 31.945862 73.398529 -9.500000
      vertex 31.732473 73.363548 -9.500000
      vertex 31.732473 73.363548 -10.500000
    endloop
  endfacet
  facet normal 0.161771 -0.986828 0.000000
    outer loop
      vertex 31.945862 73.398529 -9.500000
      vertex 31.732473 73.363548 -10.500000
      vertex 31.945862 73.398529 -10.500000
    endloop
  endfacet
  facet normal -0.054123 -0.998534 0.000000
    outer loop
      vertex 32.161785 73.386826 -9.500000
      vertex 31.945862 73.398529 -9.500000
      vertex 31.945862 73.398529 -10.500000
    endloop
  endfacet
  facet normal -0.054123 -0.998534 -0.000000
    outer loop
      vertex 32.161785 73.386826 -9.500000
      vertex 31.945862 73.398529 -10.500000
      vertex 32.161785 73.386826 -10.500000
    endloop
  endfacet
  facet normal -0.267514 -0.963554 0.000000
    outer loop
      vertex 32.370140 73.328979 -9.500000
      vertex 32.161785 73.386826 -9.500000
      vertex 32.161785 73.386826 -10.500000
    endloop
  endfacet
  facet normal -0.267514 -0.963554 -0.000000
    outer loop
      vertex 32.370140 73.328979 -9.500000
      vertex 32.161785 73.386826 -10.500000
      vertex 32.370140 73.328979 -10.500000
    endloop
  endfacet
  facet normal -0.468411 -0.883511 0.000000
    outer loop
      vertex 32.561188 73.227692 -9.500000
      vertex 32.370140 73.328979 -9.500000
      vertex 32.370140 73.328979 -10.500000
    endloop
  endfacet
  facet normal -0.468411 -0.883511 -0.000000
    outer loop
      vertex 32.561188 73.227692 -9.500000
      vertex 32.370140 73.328979 -10.500000
      vertex 32.561188 73.227692 -10.500000
    endloop
  endfacet
  facet normal -0.605196 -0.796077 0.000000
    outer loop
      vertex 32.647385 73.162163 -9.500000
      vertex 32.561188 73.227692 -9.500000
      vertex 32.561188 73.227692 -10.500000
    endloop
  endfacet
  facet normal -0.605196 -0.796077 -0.000000
    outer loop
      vertex 32.647385 73.162163 -9.500000
      vertex 32.561188 73.227692 -10.500000
      vertex 32.647385 73.162163 -10.500000
    endloop
  endfacet
  facet normal -0.725980 -0.687716 0.000000
    outer loop
      vertex 32.796093 73.005180 -9.500000
      vertex 32.647385 73.162163 -9.500000
      vertex 32.647385 73.162163 -10.500000
    endloop
  endfacet
  facet normal -0.725980 -0.687716 -0.000000
    outer loop
      vertex 32.796093 73.005180 -9.500000
      vertex 32.647385 73.162163 -10.500000
      vertex 32.796093 73.005180 -10.500000
    endloop
  endfacet
  facet normal -0.856873 -0.515528 0.000000
    outer loop
      vertex 32.907574 72.819885 -9.500000
      vertex 32.796093 73.005180 -9.500000
      vertex 32.796093 73.005180 -10.500000
    endloop
  endfacet
  facet normal -0.856873 -0.515528 -0.000000
    outer loop
      vertex 32.907574 72.819885 -9.500000
      vertex 32.796093 73.005180 -10.500000
      vertex 32.907574 72.819885 -10.500000
    endloop
  endfacet
  facet normal -0.947652 -0.319306 0.000000
    outer loop
      vertex 32.976620 72.614967 -9.500000
      vertex 32.907574 72.819885 -9.500000
      vertex 32.907574 72.819885 -10.500000
    endloop
  endfacet
  facet normal -0.947652 -0.319306 -0.000000
    outer loop
      vertex 32.976620 72.614967 -9.500000
      vertex 32.907574 72.819885 -10.500000
      vertex 32.976620 72.614967 -10.500000
    endloop
  endfacet
  facet normal -0.994137 -0.108125 0.000000
    outer loop
      vertex 33.000000 72.400002 -9.500000
      vertex 32.976620 72.614967 -9.500000
      vertex 32.976620 72.614967 -10.500000
    endloop
  endfacet
  facet normal -0.994137 -0.108125 -0.000000
    outer loop
      vertex 33.000000 72.400002 -9.500000
      vertex 32.976620 72.614967 -10.500000
      vertex 33.000000 72.400002 -10.500000
    endloop
  endfacet
  facet normal -0.994137 0.108125 0.000000
    outer loop
      vertex 32.976620 72.185036 -9.500000
      vertex 33.000000 72.400002 -9.500000
      vertex 33.000000 72.400002 -10.500000
    endloop
  endfacet
  facet normal -0.994137 0.108125 0.000000
    outer loop
      vertex 32.976620 72.185036 -9.500000
      vertex 33.000000 72.400002 -10.500000
      vertex 32.976620 72.185036 -10.500000
    endloop
  endfacet
  facet normal -0.947655 0.319296 0.000000
    outer loop
      vertex 32.907574 71.980110 -9.500000
      vertex 32.976620 72.185036 -9.500000
      vertex 32.976620 72.185036 -10.500000
    endloop
  endfacet
  facet normal -0.947655 0.319296 0.000000
    outer loop
      vertex 32.907574 71.980110 -9.500000
      vertex 32.976620 72.185036 -10.500000
      vertex 32.907574 71.980110 -10.500000
    endloop
  endfacet
  facet normal -0.856863 0.515543 0.000000
    outer loop
      vertex 32.796093 71.794823 -9.500000
      vertex 32.907574 71.980110 -9.500000
      vertex 32.907574 71.980110 -10.500000
    endloop
  endfacet
  facet normal -0.856863 0.515543 0.000000
    outer loop
      vertex 32.796093 71.794823 -9.500000
      vertex 32.907574 71.980110 -10.500000
      vertex 32.796093 71.794823 -10.500000
    endloop
  endfacet
  facet normal -0.725980 0.687716 0.000000
    outer loop
      vertex 32.647385 71.637840 -9.500000
      vertex 32.796093 71.794823 -9.500000
      vertex 32.796093 71.794823 -10.500000
    endloop
  endfacet
  facet normal -0.725980 0.687716 0.000000
    outer loop
      vertex 32.647385 71.637840 -9.500000
      vertex 32.796093 71.794823 -10.500000
      vertex 32.647385 71.637840 -10.500000
    endloop
  endfacet
  facet normal -0.605196 0.796077 0.000000
    outer loop
      vertex 32.561188 71.572311 -9.500000
      vertex 32.647385 71.637840 -9.500000
      vertex 32.647385 71.637840 -10.500000
    endloop
  endfacet
  facet normal -0.605196 0.796077 0.000000
    outer loop
      vertex 32.561188 71.572311 -9.500000
      vertex 32.647385 71.637840 -10.500000
      vertex 32.561188 71.572311 -10.500000
    endloop
  endfacet
  facet normal -0.515501 0.856889 0.000000
    outer loop
      vertex 32.468407 71.516495 -9.500000
      vertex 32.561188 71.572311 -9.500000
      vertex 32.561188 71.572311 -10.500000
    endloop
  endfacet
  facet normal -0.515501 0.856889 0.000000
    outer loop
      vertex 32.468407 71.516495 -9.500000
      vertex 32.561188 71.572311 -10.500000
      vertex 32.468407 71.516495 -10.500000
    endloop
  endfacet
  facet normal -0.370180 0.928960 0.000000
    outer loop
      vertex 32.267529 71.436447 -9.500000
      vertex 32.468407 71.516495 -9.500000
      vertex 32.468407 71.516495 -10.500000
    endloop
  endfacet
  facet normal -0.370180 0.928960 0.000000
    outer loop
      vertex 32.267529 71.436447 -9.500000
      vertex 32.468407 71.516495 -10.500000
      vertex 32.267529 71.436447 -10.500000
    endloop
  endfacet
  facet normal -0.161769 0.986829 0.000000
    outer loop
      vertex 32.054138 71.401466 -9.500000
      vertex 32.267529 71.436447 -9.500000
      vertex 32.267529 71.436447 -10.500000
    endloop
  endfacet
  facet normal -0.161769 0.986829 0.000000
    outer loop
      vertex 32.054138 71.401466 -9.500000
      vertex 32.267529 71.436447 -10.500000
      vertex 32.054138 71.401466 -10.500000
    endloop
  endfacet
  facet normal 0.054159 0.998532 0.000000
    outer loop
      vertex 31.838219 71.413177 -9.500000
      vertex 32.054138 71.401466 -9.500000
      vertex 32.054138 71.401466 -10.500000
    endloop
  endfacet
  facet normal 0.054159 0.998532 0.000000
    outer loop
      vertex 31.838219 71.413177 -9.500000
      vertex 32.054138 71.401466 -10.500000
      vertex 31.838219 71.413177 -10.500000
    endloop
  endfacet
  facet normal 0.267509 0.963555 0.000000
    outer loop
      vertex 31.629860 71.471024 -9.500000
      vertex 31.838219 71.413177 -9.500000
      vertex 31.838219 71.413177 -10.500000
    endloop
  endfacet
  facet normal 0.267509 0.963555 0.000000
    outer loop
      vertex 31.629860 71.471024 -9.500000
      vertex 31.838219 71.413177 -10.500000
      vertex 31.629860 71.471024 -10.500000
    endloop
  endfacet
  facet normal 0.468411 0.883511 0.000000
    outer loop
      vertex 31.438812 71.572311 -9.500000
      vertex 31.629860 71.471024 -9.500000
      vertex 31.629860 71.471024 -10.500000
    endloop
  endfacet
  facet normal 0.468411 0.883511 0.000000
    outer loop
      vertex 31.438812 71.572311 -9.500000
      vertex 31.629860 71.471024 -10.500000
      vertex 31.438812 71.572311 -10.500000
    endloop
  endfacet
  facet normal 0.647397 0.762153 0.000000
    outer loop
      vertex 31.274006 71.712303 -9.500000
      vertex 31.438812 71.572311 -9.500000
      vertex 31.438812 71.572311 -10.500000
    endloop
  endfacet
  facet normal 0.647397 0.762153 0.000000
    outer loop
      vertex 31.274006 71.712303 -9.500000
      vertex 31.438812 71.572311 -10.500000
      vertex 31.274006 71.712303 -10.500000
    endloop
  endfacet
  facet normal 0.796084 0.605187 0.000000
    outer loop
      vertex 31.143143 71.884445 -9.500000
      vertex 31.274006 71.712303 -9.500000
      vertex 31.274006 71.712303 -10.500000
    endloop
  endfacet
  facet normal 0.796084 0.605187 0.000000
    outer loop
      vertex 31.143143 71.884445 -9.500000
      vertex 31.274006 71.712303 -10.500000
      vertex 31.143143 71.884445 -10.500000
    endloop
  endfacet
  facet normal 0.907581 0.419876 0.000000
    outer loop
      vertex 31.052347 72.080704 -9.500000
      vertex 31.143143 71.884445 -9.500000
      vertex 31.143143 71.884445 -10.500000
    endloop
  endfacet
  facet normal 0.907581 0.419876 0.000000
    outer loop
      vertex 31.052347 72.080704 -9.500000
      vertex 31.143143 71.884445 -10.500000
      vertex 31.052347 72.080704 -10.500000
    endloop
  endfacet
  facet normal 0.976618 0.214984 0.000000
    outer loop
      vertex 31.005861 72.291878 -9.500000
      vertex 31.052347 72.080704 -9.500000
      vertex 31.052347 72.080704 -10.500000
    endloop
  endfacet
  facet normal 0.976618 0.214984 0.000000
    outer loop
      vertex 31.005861 72.291878 -9.500000
      vertex 31.052347 72.080704 -10.500000
      vertex 31.005861 72.291878 -10.500000
    endloop
  endfacet
  facet normal 0.998534 0.054130 0.000000
    outer loop
      vertex 31.000000 72.400002 -9.500000
      vertex 31.005861 72.291878 -9.500000
      vertex 31.005861 72.291878 -10.500000
    endloop
  endfacet
  facet normal 0.998534 0.054130 0.000000
    outer loop
      vertex 31.000000 72.400002 -9.500000
      vertex 31.005861 72.291878 -10.500000
      vertex 31.000000 72.400002 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.203907 73.005180 -10.500000
      vertex 31.023380 72.614967 -10.500000
      vertex 31.000000 72.400002 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -3.000000 71.199997 -10.500000
      vertex -1.043311 -0.201173 -10.500000
      vertex -1.214023 -0.229160 -10.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex -1.685486 -1.412443 -10.500000
      vertex -2.827091 -1.813473 -10.500000
      vertex -1.758123 -1.255441 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -3.000000 -1.000000 -10.500000
      vertex -1.726060 -0.664089 -10.500000
      vertex -1.781296 -0.828024 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -3.000000 -1.000000 -10.500000
      vertex -1.781296 -0.828024 -10.500000
      vertex -1.800000 -1.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -2.989044 -1.209057 -10.500000
      vertex -3.000000 -1.000000 -10.500000
      vertex -1.800000 -1.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -2.989044 -1.209057 -10.500000
      vertex -1.800000 -1.000000 -10.500000
      vertex -1.795310 -1.086495 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -2.956295 -1.415823 -10.500000
      vertex -2.989044 -1.209057 -10.500000
      vertex -1.795310 -1.086495 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -2.956295 -1.415823 -10.500000
      vertex -1.795310 -1.086495 -10.500000
      vertex -1.758123 -1.255441 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -2.902113 -1.618034 -10.500000
      vertex -2.956295 -1.415823 -10.500000
      vertex -1.758123 -1.255441 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -2.902113 -1.618034 -10.500000
      vertex -1.758123 -1.255441 -10.500000
      vertex -2.827091 -1.813473 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.100000 -3.000000 -10.500000
      vertex -0.363126 -1.484139 -10.500000
      vertex -0.273940 -1.335911 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.100000 -3.000000 -10.500000
      vertex -0.273940 -1.335911 -10.500000
      vertex -0.218704 -1.171976 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.100000 71.199997 -10.500000
      vertex -0.551050 -0.337849 -10.500000
      vertex -0.703889 -0.256819 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -3.000000 71.199997 -10.500000
      vertex -1.214023 -0.229160 -10.500000
      vertex -1.374727 -0.293190 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -3.000000 71.199997 -10.500000
      vertex -1.374727 -0.293190 -10.500000
      vertex -1.517909 -0.390270 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -3.000000 -1.000000 -10.500000
      vertex -3.000000 71.199997 -10.500000
      vertex -1.517909 -0.390270 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -3.000000 -1.000000 -10.500000
      vertex -1.517909 -0.390270 -10.500000
      vertex -1.636874 -0.515861 -10.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex -1.726060 -0.664089 -10.500000
      vertex -3.000000 -1.000000 -10.500000
      vertex -1.636874 -0.515861 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex -1.685486 -1.412443 -10.500000
      vertex -1.580796 -1.550160 -10.500000
      vertex -2.618034 -2.175570 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.685486 -1.412443 -10.500000
      vertex -2.618034 -2.175570 -10.500000
      vertex -2.732051 -2.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -2.827091 -1.813473 -10.500000
      vertex -1.685486 -1.412443 -10.500000
      vertex -2.732051 -2.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -3.000000 71.199997 -10.500000
      vertex -0.100000 71.199997 -10.500000
      vertex -0.703889 -0.256819 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -3.000000 71.199997 -10.500000
      vertex -0.703889 -0.256819 -10.500000
      vertex -0.870574 -0.210539 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.043311 -0.201173 -10.500000
      vertex -3.000000 71.199997 -10.500000
      vertex -0.870574 -0.210539 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.100000 71.199997 -10.500000
      vertex -0.218704 -0.828024 -10.500000
      vertex -0.273940 -0.664089 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.200000 -1.000000 -10.500000
      vertex -0.218704 -0.828024 -10.500000
      vertex -0.100000 71.199997 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.100000 71.199997 -10.500000
      vertex -0.273940 -0.664089 -10.500000
      vertex -0.363126 -0.515861 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.100000 71.199997 -10.500000
      vertex -0.363126 -0.515861 -10.500000
      vertex -0.482091 -0.390270 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.551050 -0.337849 -10.500000
      vertex -0.100000 71.199997 -10.500000
      vertex -0.482091 -0.390270 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.100000 -3.000000 -10.500000
      vertex -0.956689 -1.798827 -10.500000
      vertex -0.785977 -1.770840 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.100000 -3.000000 -10.500000
      vertex -0.785977 -1.770840 -10.500000
      vertex -0.625273 -1.706810 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex -1.580796 -1.550160 -10.500000
      vertex -1.448950 -1.662151 -10.500000
      vertex -2.338261 -2.486290 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.580796 -1.550160 -10.500000
      vertex -2.338261 -2.486290 -10.500000
      vertex -2.486290 -2.338261 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -2.618034 -2.175570 -10.500000
      vertex -1.580796 -1.550160 -10.500000
      vertex -2.486290 -2.338261 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex -1.448950 -1.662151 -10.500000
      vertex -1.296111 -1.743181 -10.500000
      vertex -2.000000 -2.732051 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.448950 -1.662151 -10.500000
      vertex -2.000000 -2.732051 -10.500000
      vertex -2.175570 -2.618034 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -2.338261 -2.486290 -10.500000
      vertex -1.448950 -1.662151 -10.500000
      vertex -2.175570 -2.618034 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex -1.296111 -1.743181 -10.500000
      vertex -1.129426 -1.789461 -10.500000
      vertex -1.618034 -2.902113 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.296111 -1.743181 -10.500000
      vertex -1.618034 -2.902113 -10.500000
      vertex -1.813473 -2.827091 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -2.000000 -2.732051 -10.500000
      vertex -1.296111 -1.743181 -10.500000
      vertex -1.813473 -2.827091 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex -0.956689 -1.798827 -10.500000
      vertex -0.100000 -3.000000 -10.500000
      vertex -1.000000 -3.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.956689 -1.798827 -10.500000
      vertex -1.000000 -3.000000 -10.500000
      vertex -1.209057 -2.989044 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex -1.129426 -1.789461 -10.500000
      vertex -0.956689 -1.798827 -10.500000
      vertex -1.209057 -2.989044 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.129426 -1.789461 -10.500000
      vertex -1.209057 -2.989044 -10.500000
      vertex -1.415823 -2.956295 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.618034 -2.902113 -10.500000
      vertex -1.129426 -1.789461 -10.500000
      vertex -1.415823 -2.956295 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.100000 -3.000000 -10.500000
      vertex -0.625273 -1.706810 -10.500000
      vertex -0.551050 -1.662151 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.100000 -3.000000 -10.500000
      vertex -0.551050 -1.662151 -10.500000
      vertex -0.482091 -1.609730 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex -0.363126 -1.484139 -10.500000
      vertex -0.100000 -3.000000 -10.500000
      vertex -0.482091 -1.609730 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 31.625275 -0.293190 -10.500000
      vertex 31.000000 0.000000 -10.500000
      vertex 31.785976 -0.229160 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.100000 71.199997 -10.500000
      vertex 31.000000 71.000000 -10.500000
      vertex -0.000000 71.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.100000 -3.000000 -10.500000
      vertex -0.218704 -1.171976 -10.500000
      vertex -0.200000 -1.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.100000 -3.000000 -10.500000
      vertex -0.200000 -1.000000 -10.500000
      vertex -0.100000 71.199997 -10.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 0.000000 0.000000 -10.500000
      vertex -0.100000 -3.000000 -10.500000
      vertex -0.100000 71.199997 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 0.000000 0.000000 -10.500000
      vertex -0.100000 71.199997 -10.500000
      vertex -0.000000 71.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 31.000000 0.000000 -10.500000
      vertex 31.625275 -0.293190 -10.500000
      vertex 31.482090 -0.390270 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 31.000000 0.000000 -10.500000
      vertex 31.482090 -0.390270 -10.500000
      vertex 31.363127 -0.515861 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 28.000000 0.000000 -10.500000
      vertex 31.000000 0.000000 -10.500000
      vertex 31.363127 -0.515861 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 28.000000 0.000000 -10.500000
      vertex 31.363127 -0.515861 -10.500000
      vertex 31.273939 -0.664089 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 28.000000 0.000000 -10.500000
      vertex 31.273939 -0.664089 -10.500000
      vertex 31.218704 -0.828024 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 28.000000 -1.000000 -10.500000
      vertex 28.000000 0.000000 -10.500000
      vertex 31.218704 -0.828024 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 33.989040 -1.209057 -10.500000
      vertex 32.799999 -1.000000 -10.500000
      vertex 34.000000 -1.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 31.000000 0.000000 -10.500000
      vertex 31.000000 71.000000 -10.500000
      vertex 32.129425 -0.210539 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 31.000000 0.000000 -10.500000
      vertex 32.129425 -0.210539 -10.500000
      vertex 31.956688 -0.201173 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 31.785976 -0.229160 -10.500000
      vertex 31.000000 0.000000 -10.500000
      vertex 31.956688 -0.201173 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.100000 -3.000000 -10.500000
      vertex 0.000000 0.000000 -10.500000
      vertex 3.000000 0.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.100000 -3.000000 -10.500000
      vertex 3.000000 0.000000 -10.500000
      vertex 3.000000 -1.000000 -10.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 28.000000 -1.000000 -10.500000
      vertex -0.100000 -3.000000 -10.500000
      vertex 3.000000 -1.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 31.419203 -1.550160 -10.500000
      vertex 31.551052 -1.662151 -10.500000
      vertex 32.000000 -3.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 31.419203 -1.550160 -10.500000
      vertex 32.000000 -3.000000 -10.500000
      vertex -0.100000 -3.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 31.314514 -1.412443 -10.500000
      vertex 31.419203 -1.550160 -10.500000
      vertex -0.100000 -3.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.781296 -1.171976 -10.500000
      vertex 32.799999 -1.000000 -10.500000
      vertex 33.989040 -1.209057 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 28.000000 -1.000000 -10.500000
      vertex 31.218704 -0.828024 -10.500000
      vertex 31.199999 -1.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 28.000000 -1.000000 -10.500000
      vertex 31.199999 -1.000000 -10.500000
      vertex 31.204689 -1.086495 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.100000 -3.000000 -10.500000
      vertex 28.000000 -1.000000 -10.500000
      vertex 31.204689 -1.086495 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.100000 -3.000000 -10.500000
      vertex 31.204689 -1.086495 -10.500000
      vertex 31.241877 -1.255441 -10.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 31.314514 -1.412443 -10.500000
      vertex -0.100000 -3.000000 -10.500000
      vertex 31.241877 -1.255441 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 33.732048 -2.000000 -10.500000
      vertex 32.636875 -1.484139 -10.500000
      vertex 32.726059 -1.335911 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.781296 -1.171976 -10.500000
      vertex 33.989040 -1.209057 -10.500000
      vertex 33.956295 -1.415823 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.781296 -1.171976 -10.500000
      vertex 33.956295 -1.415823 -10.500000
      vertex 33.902111 -1.618034 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.726059 -1.335911 -10.500000
      vertex 32.781296 -1.171976 -10.500000
      vertex 33.902111 -1.618034 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.726059 -1.335911 -10.500000
      vertex 33.902111 -1.618034 -10.500000
      vertex 33.827091 -1.813473 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 33.732048 -2.000000 -10.500000
      vertex 32.726059 -1.335911 -10.500000
      vertex 33.827091 -1.813473 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 -3.000000 -10.500000
      vertex 31.551052 -1.662151 -10.500000
      vertex 31.703890 -1.743181 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 -3.000000 -10.500000
      vertex 31.703890 -1.743181 -10.500000
      vertex 31.870573 -1.789461 -10.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 32.209057 -2.989044 -10.500000
      vertex 32.000000 -3.000000 -10.500000
      vertex 31.870573 -1.789461 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.209057 -2.989044 -10.500000
      vertex 31.870573 -1.789461 -10.500000
      vertex 32.043312 -1.798827 -10.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 32.415821 -2.956295 -10.500000
      vertex 32.209057 -2.989044 -10.500000
      vertex 32.043312 -1.798827 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.415821 -2.956295 -10.500000
      vertex 32.043312 -1.798827 -10.500000
      vertex 32.214024 -1.770840 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.374729 -1.706810 -10.500000
      vertex 32.448952 -1.662151 -10.500000
      vertex 33.000000 -2.732051 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.374729 -1.706810 -10.500000
      vertex 33.000000 -2.732051 -10.500000
      vertex 32.813473 -2.827091 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.214024 -1.770840 -10.500000
      vertex 32.374729 -1.706810 -10.500000
      vertex 32.813473 -2.827091 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.214024 -1.770840 -10.500000
      vertex 32.813473 -2.827091 -10.500000
      vertex 32.618034 -2.902113 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.415821 -2.956295 -10.500000
      vertex 32.214024 -1.770840 -10.500000
      vertex 32.618034 -2.902113 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.636875 -1.484139 -10.500000
      vertex 33.732048 -2.000000 -10.500000
      vertex 33.618034 -2.175570 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.636875 -1.484139 -10.500000
      vertex 33.618034 -2.175570 -10.500000
      vertex 33.486286 -2.338261 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.517910 -1.609730 -10.500000
      vertex 32.636875 -1.484139 -10.500000
      vertex 33.486286 -2.338261 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.517910 -1.609730 -10.500000
      vertex 33.486286 -2.338261 -10.500000
      vertex 33.338261 -2.486290 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.448952 -1.662151 -10.500000
      vertex 32.517910 -1.609730 -10.500000
      vertex 33.338261 -2.486290 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.448952 -1.662151 -10.500000
      vertex 33.338261 -2.486290 -10.500000
      vertex 33.175568 -2.618034 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 33.000000 -2.732051 -10.500000
      vertex 32.448952 -1.662151 -10.500000
      vertex 33.175568 -2.618034 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 34.000000 71.199997 -10.500000
      vertex 32.448952 -0.337849 -10.500000
      vertex 32.296108 -0.256819 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.517910 -0.390270 -10.500000
      vertex 32.448952 -0.337849 -10.500000
      vertex 34.000000 71.199997 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 34.000000 -1.000000 -10.500000
      vertex 32.799999 -1.000000 -10.500000
      vertex 32.781296 -0.828024 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 34.000000 -1.000000 -10.500000
      vertex 32.781296 -0.828024 -10.500000
      vertex 32.726059 -0.664089 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 34.000000 71.199997 -10.500000
      vertex 34.000000 -1.000000 -10.500000
      vertex 32.726059 -0.664089 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 34.000000 71.199997 -10.500000
      vertex 32.726059 -0.664089 -10.500000
      vertex 32.636875 -0.515861 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.517910 -0.390270 -10.500000
      vertex 34.000000 71.199997 -10.500000
      vertex 32.636875 -0.515861 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.092425 72.819885 -10.500000
      vertex -0.203907 73.005180 -10.500000
      vertex 31.000000 72.400002 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 32.267529 71.436447 -10.500000
      vertex 34.000000 71.199997 -10.500000
      vertex 32.054138 71.401466 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 31.732473 73.363548 -10.500000
      vertex 32.000000 74.000000 -10.500000
      vertex 31.945862 73.398529 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 31.629860 71.471024 -10.500000
      vertex 31.838219 71.413177 -10.500000
      vertex -0.100000 71.199997 -10.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 31.629860 71.471024 -10.500000
      vertex -0.100000 71.199997 -10.500000
      vertex 31.438812 71.572311 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.100000 71.199997 -10.500000
      vertex 31.838219 71.413177 -10.500000
      vertex 32.054138 71.401466 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.100000 71.199997 -10.500000
      vertex 32.054138 71.401466 -10.500000
      vertex 34.000000 71.199997 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 31.000000 71.000000 -10.500000
      vertex -0.100000 71.199997 -10.500000
      vertex 34.000000 71.199997 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 31.000000 71.000000 -10.500000
      vertex 34.000000 71.199997 -10.500000
      vertex 32.296108 -0.256819 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.129425 -0.210539 -10.500000
      vertex 31.000000 71.000000 -10.500000
      vertex 32.296108 -0.256819 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 31.274006 71.712303 -10.500000
      vertex 31.438812 71.572311 -10.500000
      vertex -0.100000 71.199997 -10.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 31.274006 71.712303 -10.500000
      vertex -0.100000 71.199997 -10.500000
      vertex -0.203907 71.794823 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex -0.092425 71.980110 -10.500000
      vertex 31.274006 71.712303 -10.500000
      vertex -0.203907 71.794823 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.100000 74.000000 -10.500000
      vertex 31.352613 73.162163 -10.500000
      vertex 31.203907 73.005180 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.100000 74.000000 -10.500000
      vertex 31.203907 73.005180 -10.500000
      vertex 31.092424 72.819885 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 31.023380 72.614967 -10.500000
      vertex -0.100000 74.000000 -10.500000
      vertex 31.092424 72.819885 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 34.000000 71.199997 -10.500000
      vertex 32.267529 71.436447 -10.500000
      vertex 32.468407 71.516495 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 34.000000 71.199997 -10.500000
      vertex 32.468407 71.516495 -10.500000
      vertex 32.561188 71.572311 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 32.647385 71.637840 -10.500000
      vertex 34.000000 71.199997 -10.500000
      vertex 32.561188 71.572311 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.100000 74.000000 -10.500000
      vertex 32.000000 74.000000 -10.500000
      vertex 31.732473 73.363548 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.100000 74.000000 -10.500000
      vertex 31.732473 73.363548 -10.500000
      vertex 31.531591 73.283508 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 31.352613 73.162163 -10.500000
      vertex -0.100000 74.000000 -10.500000
      vertex 31.531591 73.283508 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.796093 73.005180 -10.500000
      vertex 33.486286 73.338264 -10.500000
      vertex 32.907574 72.819885 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.161785 73.386826 -10.500000
      vertex 32.415821 73.956299 -10.500000
      vertex 32.370140 73.328979 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.161785 73.386826 -10.500000
      vertex 31.945862 73.398529 -10.500000
      vertex 32.000000 74.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.161785 73.386826 -10.500000
      vertex 32.000000 74.000000 -10.500000
      vertex 32.209057 73.989044 -10.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 32.415821 73.956299 -10.500000
      vertex 32.161785 73.386826 -10.500000
      vertex 32.209057 73.989044 -10.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 31.000000 72.400002 -10.500000
      vertex -0.023379 72.185036 -10.500000
      vertex -0.000000 72.400002 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 31.000000 72.400002 -10.500000
      vertex -0.000000 72.400002 -10.500000
      vertex -0.023379 72.614967 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.092425 72.819885 -10.500000
      vertex 31.000000 72.400002 -10.500000
      vertex -0.023379 72.614967 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 34.000000 71.199997 -10.500000
      vertex 32.647385 71.637840 -10.500000
      vertex 32.796093 71.794823 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 34.000000 71.199997 -10.500000
      vertex 32.796093 71.794823 -10.500000
      vertex 32.907574 71.980110 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 34.000000 72.000000 -10.500000
      vertex 34.000000 71.199997 -10.500000
      vertex 32.907574 71.980110 -10.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 34.000000 72.000000 -10.500000
      vertex 32.907574 71.980110 -10.500000
      vertex 32.976620 72.185036 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 33.989040 72.209061 -10.500000
      vertex 34.000000 72.000000 -10.500000
      vertex 32.976620 72.185036 -10.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 33.989040 72.209061 -10.500000
      vertex 32.976620 72.185036 -10.500000
      vertex 33.000000 72.400002 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 33.000000 72.400002 -10.500000
      vertex 32.976620 72.614967 -10.500000
      vertex 33.902111 72.618034 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 33.000000 72.400002 -10.500000
      vertex 33.902111 72.618034 -10.500000
      vertex 33.956295 72.415825 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 33.989040 72.209061 -10.500000
      vertex 33.000000 72.400002 -10.500000
      vertex 33.956295 72.415825 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.907574 72.819885 -10.500000
      vertex 33.486286 73.338264 -10.500000
      vertex 33.618034 73.175575 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.907574 72.819885 -10.500000
      vertex 33.618034 73.175575 -10.500000
      vertex 33.732048 73.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.976620 72.614967 -10.500000
      vertex 32.907574 72.819885 -10.500000
      vertex 33.732048 73.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.976620 72.614967 -10.500000
      vertex 33.732048 73.000000 -10.500000
      vertex 33.827091 72.813477 -10.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 33.902111 72.618034 -10.500000
      vertex 32.976620 72.614967 -10.500000
      vertex 33.827091 72.813477 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.370140 73.328979 -10.500000
      vertex 32.415821 73.956299 -10.500000
      vertex 32.618034 73.902115 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.370140 73.328979 -10.500000
      vertex 32.618034 73.902115 -10.500000
      vertex 32.813473 73.827087 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.561188 73.227692 -10.500000
      vertex 32.370140 73.328979 -10.500000
      vertex 32.813473 73.827087 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.561188 73.227692 -10.500000
      vertex 32.813473 73.827087 -10.500000
      vertex 33.000000 73.732048 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.647385 73.162163 -10.500000
      vertex 32.561188 73.227692 -10.500000
      vertex 33.000000 73.732048 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.647385 73.162163 -10.500000
      vertex 33.000000 73.732048 -10.500000
      vertex 33.175568 73.618034 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.796093 73.005180 -10.500000
      vertex 32.647385 73.162163 -10.500000
      vertex 33.175568 73.618034 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.796093 73.005180 -10.500000
      vertex 33.175568 73.618034 -10.500000
      vertex 33.338261 73.486290 -10.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 33.486286 73.338264 -10.500000
      vertex 32.796093 73.005180 -10.500000
      vertex 33.338261 73.486290 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.023379 72.185036 -10.500000
      vertex 31.000000 72.400002 -10.500000
      vertex 31.005861 72.291878 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.023379 72.185036 -10.500000
      vertex 31.005861 72.291878 -10.500000
      vertex 31.052347 72.080704 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.092425 71.980110 -10.500000
      vertex -0.023379 72.185036 -10.500000
      vertex 31.052347 72.080704 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.092425 71.980110 -10.500000
      vertex 31.052347 72.080704 -10.500000
      vertex 31.143143 71.884445 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 31.274006 71.712303 -10.500000
      vertex -0.092425 71.980110 -10.500000
      vertex 31.143143 71.884445 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.100000 74.000000 -10.500000
      vertex -0.438813 73.227692 -10.500000
      vertex -0.629862 73.328979 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 74.000000 -10.500000
      vertex -0.100000 74.000000 -10.500000
      vertex -0.629862 73.328979 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex -0.100000 74.000000 -10.500000
      vertex 31.023380 72.614967 -10.500000
      vertex -0.203907 73.005180 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.100000 74.000000 -10.500000
      vertex -0.203907 73.005180 -10.500000
      vertex -0.352614 73.162163 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.438813 73.227692 -10.500000
      vertex -0.100000 74.000000 -10.500000
      vertex -0.352614 73.162163 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 74.000000 -10.500000
      vertex -0.629862 73.328979 -10.500000
      vertex -0.838218 73.386826 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex -1.000000 74.000000 -10.500000
      vertex -0.838218 73.386826 -10.500000
      vertex -1.054139 73.398529 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.209057 73.989044 -10.500000
      vertex -1.000000 74.000000 -10.500000
      vertex -1.054139 73.398529 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex -1.209057 73.989044 -10.500000
      vertex -1.054139 73.398529 -10.500000
      vertex -1.267528 73.363548 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.100000 71.199997 -10.500000
      vertex -0.945861 71.401466 -10.500000
      vertex -0.732472 71.436447 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.100000 71.199997 -10.500000
      vertex -0.732472 71.436447 -10.500000
      vertex -0.531592 71.516495 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.161782 71.413177 -10.500000
      vertex -0.945861 71.401466 -10.500000
      vertex -0.100000 71.199997 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex -1.161782 71.413177 -10.500000
      vertex -0.100000 71.199997 -10.500000
      vertex -3.000000 71.199997 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex -1.370138 71.471024 -10.500000
      vertex -1.161782 71.413177 -10.500000
      vertex -3.000000 71.199997 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.100000 71.199997 -10.500000
      vertex -0.531592 71.516495 -10.500000
      vertex -0.438813 71.572311 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.100000 71.199997 -10.500000
      vertex -0.438813 71.572311 -10.500000
      vertex -0.352614 71.637840 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex -0.203907 71.794823 -10.500000
      vertex -0.100000 71.199997 -10.500000
      vertex -0.352614 71.637840 -10.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex -1.647386 73.162163 -10.500000
      vertex -1.796093 73.005180 -10.500000
      vertex -2.175570 73.618034 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.647386 73.162163 -10.500000
      vertex -2.175570 73.618034 -10.500000
      vertex -2.000000 73.732048 -10.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex -1.468408 73.283508 -10.500000
      vertex -1.647386 73.162163 -10.500000
      vertex -2.000000 73.732048 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.468408 73.283508 -10.500000
      vertex -2.000000 73.732048 -10.500000
      vertex -1.813473 73.827087 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.468408 73.283508 -10.500000
      vertex -1.813473 73.827087 -10.500000
      vertex -1.618034 73.902115 -10.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex -1.267528 73.363548 -10.500000
      vertex -1.468408 73.283508 -10.500000
      vertex -1.618034 73.902115 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.267528 73.363548 -10.500000
      vertex -1.618034 73.902115 -10.500000
      vertex -1.415823 73.956299 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.209057 73.989044 -10.500000
      vertex -1.267528 73.363548 -10.500000
      vertex -1.415823 73.956299 -10.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex -1.796093 73.005180 -10.500000
      vertex -1.907575 72.819885 -10.500000
      vertex -2.486290 73.338264 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.796093 73.005180 -10.500000
      vertex -2.486290 73.338264 -10.500000
      vertex -2.338261 73.486290 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex -2.175570 73.618034 -10.500000
      vertex -1.796093 73.005180 -10.500000
      vertex -2.338261 73.486290 -10.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex -1.907575 72.819885 -10.500000
      vertex -1.976621 72.614967 -10.500000
      vertex -2.732051 73.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.907575 72.819885 -10.500000
      vertex -2.732051 73.000000 -10.500000
      vertex -2.618034 73.175575 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex -2.486290 73.338264 -10.500000
      vertex -1.907575 72.819885 -10.500000
      vertex -2.618034 73.175575 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -3.000000 71.199997 -10.500000
      vertex -1.856857 71.884445 -10.500000
      vertex -1.725995 71.712303 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -3.000000 71.199997 -10.500000
      vertex -1.725995 71.712303 -10.500000
      vertex -1.561187 71.572311 -10.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex -1.370138 71.471024 -10.500000
      vertex -3.000000 71.199997 -10.500000
      vertex -1.561187 71.572311 -10.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex -1.976621 72.614967 -10.500000
      vertex -2.000000 72.400002 -10.500000
      vertex -2.902113 72.618034 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.976621 72.614967 -10.500000
      vertex -2.902113 72.618034 -10.500000
      vertex -2.827091 72.813477 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex -2.732051 73.000000 -10.500000
      vertex -1.976621 72.614967 -10.500000
      vertex -2.827091 72.813477 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex -1.947653 72.080704 -10.500000
      vertex -1.856857 71.884445 -10.500000
      vertex -3.000000 71.199997 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.947653 72.080704 -10.500000
      vertex -3.000000 71.199997 -10.500000
      vertex -3.000000 72.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex -1.994138 72.291878 -10.500000
      vertex -1.947653 72.080704 -10.500000
      vertex -3.000000 72.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.994138 72.291878 -10.500000
      vertex -3.000000 72.000000 -10.500000
      vertex -2.989044 72.209061 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex -2.000000 72.400002 -10.500000
      vertex -1.994138 72.291878 -10.500000
      vertex -2.989044 72.209061 -10.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex -2.000000 72.400002 -10.500000
      vertex -2.989044 72.209061 -10.500000
      vertex -2.956295 72.415825 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex -2.902113 72.618034 -10.500000
      vertex -2.000000 72.400002 -10.500000
      vertex -2.956295 72.415825 -10.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 72.400002 -9.500000
      vertex 31.000000 72.400002 -9.500000
      vertex 31.023380 72.614967 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 72.400002 -9.500000
      vertex 31.143143 71.884445 -9.500000
      vertex 31.052347 72.080704 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 72.400002 -9.500000
      vertex 31.052347 72.080704 -9.500000
      vertex 31.005861 72.291878 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 31.000000 72.400002 -9.500000
      vertex 32.000000 72.400002 -9.500000
      vertex 31.005861 72.291878 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 72.400002 -9.500000
      vertex 31.629860 71.471024 -9.500000
      vertex 31.438812 71.572311 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 72.400002 -9.500000
      vertex 31.438812 71.572311 -9.500000
      vertex 31.274006 71.712303 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 31.143143 71.884445 -9.500000
      vertex 32.000000 72.400002 -9.500000
      vertex 31.274006 71.712303 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 72.400002 -9.500000
      vertex 32.267529 71.436447 -9.500000
      vertex 32.054138 71.401466 -9.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 32.000000 72.400002 -9.500000
      vertex 32.054138 71.401466 -9.500000
      vertex 31.838219 71.413177 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 31.629860 71.471024 -9.500000
      vertex 32.000000 72.400002 -9.500000
      vertex 31.838219 71.413177 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 72.400002 -9.500000
      vertex 32.647385 71.637840 -9.500000
      vertex 32.561188 71.572311 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 72.400002 -9.500000
      vertex 32.561188 71.572311 -9.500000
      vertex 32.468407 71.516495 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.267529 71.436447 -9.500000
      vertex 32.000000 72.400002 -9.500000
      vertex 32.468407 71.516495 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 72.400002 -9.500000
      vertex 32.976620 72.185036 -9.500000
      vertex 32.907574 71.980110 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 72.400002 -9.500000
      vertex 32.907574 71.980110 -9.500000
      vertex 32.796093 71.794823 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.647385 71.637840 -9.500000
      vertex 32.000000 72.400002 -9.500000
      vertex 32.796093 71.794823 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 72.400002 -9.500000
      vertex 32.907574 72.819885 -9.500000
      vertex 32.976620 72.614967 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 72.400002 -9.500000
      vertex 32.976620 72.614967 -9.500000
      vertex 33.000000 72.400002 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.976620 72.185036 -9.500000
      vertex 32.000000 72.400002 -9.500000
      vertex 33.000000 72.400002 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 72.400002 -9.500000
      vertex 32.561188 73.227692 -9.500000
      vertex 32.647385 73.162163 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 72.400002 -9.500000
      vertex 32.647385 73.162163 -9.500000
      vertex 32.796093 73.005180 -9.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 32.907574 72.819885 -9.500000
      vertex 32.000000 72.400002 -9.500000
      vertex 32.796093 73.005180 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 72.400002 -9.500000
      vertex 31.945862 73.398529 -9.500000
      vertex 32.161785 73.386826 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 72.400002 -9.500000
      vertex 32.161785 73.386826 -9.500000
      vertex 32.370140 73.328979 -9.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 32.561188 73.227692 -9.500000
      vertex 32.000000 72.400002 -9.500000
      vertex 32.370140 73.328979 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 72.400002 -9.500000
      vertex 31.352613 73.162163 -9.500000
      vertex 31.531591 73.283508 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 72.400002 -9.500000
      vertex 31.531591 73.283508 -9.500000
      vertex 31.732473 73.363548 -9.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 31.945862 73.398529 -9.500000
      vertex 32.000000 72.400002 -9.500000
      vertex 31.732473 73.363548 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 72.400002 -9.500000
      vertex 31.023380 72.614967 -9.500000
      vertex 31.092424 72.819885 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 32.000000 72.400002 -9.500000
      vertex 31.092424 72.819885 -9.500000
      vertex 31.203907 73.005180 -9.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 31.352613 73.162163 -9.500000
      vertex 32.000000 72.400002 -9.500000
      vertex 31.203907 73.005180 -9.500000
    endloop
  endfacet
  facet normal 0.000000 -0.182241 0.983254
    outer loop
      vertex 18.424623 -1.312869 12.475377
      vertex 9.856295 -1.415823 12.456295
      vertex 18.443705 -1.415823 12.456295
    endloop
  endfacet
  facet normal 0.000000 -0.026176 0.999657
    outer loop
      vertex 18.402740 -1.104672 12.497259
      vertex 18.400000 -1.000000 12.500000
      vertex 9.900000 -1.000000 12.500000
    endloop
  endfacet
  facet normal 0.000000 -0.026176 0.999657
    outer loop
      vertex 18.402740 -1.104672 12.497259
      vertex 9.900000 -1.000000 12.500000
      vertex 9.897259 -1.104672 12.497259
    endloop
  endfacet
  facet normal 0.000000 -0.078456 0.996918
    outer loop
      vertex 18.410957 -1.209057 12.489044
      vertex 18.402740 -1.104672 12.497259
      vertex 9.897259 -1.104672 12.497259
    endloop
  endfacet
  facet normal 0.000000 -0.078456 0.996918
    outer loop
      vertex 18.410957 -1.209057 12.489044
      vertex 9.897259 -1.104672 12.497259
      vertex 9.889044 -1.209057 12.489044
    endloop
  endfacet
  facet normal 0.000000 -0.130526 0.991445
    outer loop
      vertex 18.424623 -1.312869 12.475377
      vertex 18.410957 -1.209057 12.489044
      vertex 9.889044 -1.209057 12.489044
    endloop
  endfacet
  facet normal 0.000000 -0.130526 0.991445
    outer loop
      vertex 18.424623 -1.312869 12.475377
      vertex 9.889044 -1.209057 12.489044
      vertex 9.875377 -1.312869 12.475377
    endloop
  endfacet
  facet normal 0.000000 -0.182241 0.983254
    outer loop
      vertex 9.856295 -1.415823 12.456295
      vertex 18.424623 -1.312869 12.475377
      vertex 9.875377 -1.312869 12.475377
    endloop
  endfacet
  facet normal 0.000000 -0.233446 0.972370
    outer loop
      vertex 18.468149 -1.517638 12.431851
      vertex 18.443705 -1.415823 12.456295
      vertex 9.856295 -1.415823 12.456295
    endloop
  endfacet
  facet normal 0.000000 -0.233446 0.972370
    outer loop
      vertex 18.468149 -1.517638 12.431851
      vertex 9.856295 -1.415823 12.456295
      vertex 9.831851 -1.517638 12.431851
    endloop
  endfacet
  facet normal 0.000000 -0.284014 0.958820
    outer loop
      vertex 18.497887 -1.618034 12.402113
      vertex 18.468149 -1.517638 12.431851
      vertex 9.831851 -1.517638 12.431851
    endloop
  endfacet
  facet normal 0.000000 -0.284014 0.958820
    outer loop
      vertex 18.497887 -1.618034 12.402113
      vertex 9.831851 -1.517638 12.431851
      vertex 9.802114 -1.618034 12.402113
    endloop
  endfacet
  facet normal 0.000000 -0.333807 0.942641
    outer loop
      vertex 18.532839 -1.716736 12.367161
      vertex 18.497887 -1.618034 12.402113
      vertex 9.802114 -1.618034 12.402113
    endloop
  endfacet
  facet normal 0.000000 -0.333807 0.942641
    outer loop
      vertex 18.532839 -1.716736 12.367161
      vertex 9.802114 -1.618034 12.402113
      vertex 9.767160 -1.716736 12.367161
    endloop
  endfacet
  facet normal 0.000000 -0.382680 0.923881
    outer loop
      vertex 18.572910 -1.813473 12.327091
      vertex 18.532839 -1.716736 12.367161
      vertex 9.767160 -1.716736 12.367161
    endloop
  endfacet
  facet normal 0.000000 -0.382680 0.923881
    outer loop
      vertex 18.572910 -1.813473 12.327091
      vertex 9.767160 -1.716736 12.367161
      vertex 9.727091 -1.813473 12.327091
    endloop
  endfacet
  facet normal 0.000000 -0.430514 0.902584
    outer loop
      vertex 18.617989 -1.907981 12.282013
      vertex 18.572910 -1.813473 12.327091
      vertex 9.727091 -1.813473 12.327091
    endloop
  endfacet
  facet normal 0.000000 -0.430514 0.902584
    outer loop
      vertex 18.617989 -1.907981 12.282013
      vertex 9.727091 -1.813473 12.327091
      vertex 9.682013 -1.907981 12.282013
    endloop
  endfacet
  facet normal 0.000000 -0.477157 0.878818
    outer loop
      vertex 18.667950 -2.000000 12.232051
      vertex 18.617989 -1.907981 12.282013
      vertex 9.682013 -1.907981 12.282013
    endloop
  endfacet
  facet normal 0.000000 -0.477157 0.878818
    outer loop
      vertex 18.667950 -2.000000 12.232051
      vertex 9.682013 -1.907981 12.282013
      vertex 9.632051 -2.000000 12.232051
    endloop
  endfacet
  facet normal 0.000000 -0.522504 0.852637
    outer loop
      vertex 18.722658 -2.089278 12.177341
      vertex 18.667950 -2.000000 12.232051
      vertex 9.632051 -2.000000 12.232051
    endloop
  endfacet
  facet normal 0.000000 -0.522504 0.852637
    outer loop
      vertex 18.722658 -2.089278 12.177341
      vertex 9.632051 -2.000000 12.232051
      vertex 9.577341 -2.089278 12.177341
    endloop
  endfacet
  facet normal 0.000000 -0.566399 0.824131
    outer loop
      vertex 18.722658 -2.089278 12.177341
      vertex 9.577341 -2.089278 12.177341
      vertex 9.518034 -2.175570 12.118034
    endloop
  endfacet
  facet normal 0.000000 -0.566399 0.824131
    outer loop
      vertex 18.781965 -2.175570 12.118034
      vertex 18.722658 -2.089278 12.177341
      vertex 9.518034 -2.175570 12.118034
    endloop
  endfacet
  facet normal 0.000000 -0.629321 0.777146
    outer loop
      vertex 18.781965 -2.175570 12.118034
      vertex 9.518034 -2.175570 12.118034
      vertex 9.386290 -2.338261 11.986290
    endloop
  endfacet
  facet normal 0.000000 -0.629321 0.777146
    outer loop
      vertex 18.913710 -2.338261 11.986290
      vertex 18.781965 -2.175570 12.118034
      vertex 9.386290 -2.338261 11.986290
    endloop
  endfacet
  facet normal 0.000000 -0.707108 0.707105
    outer loop
      vertex 18.913710 -2.338261 11.986290
      vertex 9.386290 -2.338261 11.986290
      vertex 9.238261 -2.486290 11.838261
    endloop
  endfacet
  facet normal 0.000000 -0.707108 0.707105
    outer loop
      vertex 19.061739 -2.486290 11.838261
      vertex 18.913710 -2.338261 11.986290
      vertex 9.238261 -2.486290 11.838261
    endloop
  endfacet
  facet normal 0.000000 -0.777145 0.629321
    outer loop
      vertex 19.061739 -2.486290 11.838261
      vertex 9.238261 -2.486290 11.838261
      vertex 9.075571 -2.618034 11.675570
    endloop
  endfacet
  facet normal 0.000000 -0.777145 0.629321
    outer loop
      vertex 19.224430 -2.618034 11.675570
      vertex 19.061739 -2.486290 11.838261
      vertex 9.075571 -2.618034 11.675570
    endloop
  endfacet
  facet normal 0.000000 -0.838670 0.544640
    outer loop
      vertex 19.224430 -2.618034 11.675570
      vertex 9.075571 -2.618034 11.675570
      vertex 8.900000 -2.732051 11.500000
    endloop
  endfacet
  facet normal 0.000000 -0.838670 0.544640
    outer loop
      vertex 19.400002 -2.732051 11.500000
      vertex 19.224430 -2.618034 11.675570
      vertex 8.900000 -2.732051 11.500000
    endloop
  endfacet
  facet normal 0.000000 -0.891007 0.453989
    outer loop
      vertex 19.400002 -2.732051 11.500000
      vertex 8.900000 -2.732051 11.500000
      vertex 8.713473 -2.827091 11.313473
    endloop
  endfacet
  facet normal 0.000000 -0.891007 0.453989
    outer loop
      vertex 19.586525 -2.827091 11.313473
      vertex 19.400002 -2.732051 11.500000
      vertex 8.713473 -2.827091 11.313473
    endloop
  endfacet
  facet normal 0.000000 -0.933580 0.358370
    outer loop
      vertex 19.586525 -2.827091 11.313473
      vertex 8.713473 -2.827091 11.313473
      vertex 8.518034 -2.902113 11.118034
    endloop
  endfacet
  facet normal 0.000000 -0.933580 0.358370
    outer loop
      vertex 19.781965 -2.902113 11.118034
      vertex 19.586525 -2.827091 11.313473
      vertex 8.518034 -2.902113 11.118034
    endloop
  endfacet
  facet normal 0.000000 -0.965926 0.258818
    outer loop
      vertex 19.781965 -2.902113 11.118034
      vertex 8.518034 -2.902113 11.118034
      vertex 8.315823 -2.956295 10.915823
    endloop
  endfacet
  facet normal 0.000000 -0.965926 0.258818
    outer loop
      vertex 19.984177 -2.956295 10.915823
      vertex 19.781965 -2.902113 11.118034
      vertex 8.315823 -2.956295 10.915823
    endloop
  endfacet
  facet normal 0.000000 -0.987688 0.156434
    outer loop
      vertex 19.984177 -2.956295 10.915823
      vertex 8.315823 -2.956295 10.915823
      vertex 8.109057 -2.989044 10.709057
    endloop
  endfacet
  facet normal 0.000000 -0.987688 0.156434
    outer loop
      vertex 20.190943 -2.989044 10.709057
      vertex 19.984177 -2.956295 10.915823
      vertex 8.109057 -2.989044 10.709057
    endloop
  endfacet
  facet normal 0.000000 -0.998630 0.052336
    outer loop
      vertex 20.190943 -2.989044 10.709057
      vertex 8.109057 -2.989044 10.709057
      vertex 7.900000 -3.000000 10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.998630 0.052336
    outer loop
      vertex 20.400002 -3.000000 10.500000
      vertex 20.190943 -2.989044 10.709057
      vertex 7.900000 -3.000000 10.500000
    endloop
  endfacet
  facet normal 1.000000 0.000000 0.000000
    outer loop
      vertex 34.000000 71.199997 -10.500000
      vertex 34.000000 72.000000 -10.500000
      vertex 34.000000 72.000000 23.000000
    endloop
  endfacet
  facet normal 1.000000 0.000000 -0.000000
    outer loop
      vertex 34.000000 71.199997 -10.500000
      vertex 34.000000 72.000000 23.000000
      vertex 34.000000 71.099998 23.000000
    endloop
  endfacet
  facet normal 1.000000 0.000000 0.000000
    outer loop
      vertex 34.000000 -1.000000 -10.500000
      vertex 34.000000 71.199997 -10.500000
      vertex 34.000000 71.099998 23.000000
    endloop
  endfacet
  facet normal 1.000000 0.000000 0.000000
    outer loop
      vertex 34.000000 -1.000000 -10.500000
      vertex 34.000000 71.099998 23.000000
      vertex 34.000000 -1.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 3.000000 -1.000000 0.000000
      vertex 7.750000 -1.000000 -4.500000
      vertex 3.000000 -1.000000 -4.500000
    endloop
  endfacet
  facet normal -0.000000 1.000000 0.000000
    outer loop
      vertex 23.250000 -1.000000 -6.500000
      vertex 28.000000 -1.000000 -6.500000
      vertex 28.000000 -1.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 23.250000 -1.000000 -6.500000
      vertex 28.000000 -1.000000 -10.500000
      vertex 3.000000 -1.000000 -10.500000
    endloop
  endfacet
  facet normal -0.000000 1.000000 0.000000
    outer loop
      vertex 7.750000 -1.000000 -6.500000
      vertex 23.250000 -1.000000 -6.500000
      vertex 3.000000 -1.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 7.750000 -1.000000 -6.500000
      vertex 3.000000 -1.000000 -10.500000
      vertex 3.000000 -1.000000 -6.500000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 23.250000 -1.000000 -4.500000
      vertex 28.000000 -1.000000 0.000000
      vertex 28.000000 -1.000000 -4.500000
    endloop
  endfacet
  facet normal 0.000000 1.000000 -0.000000
    outer loop
      vertex 7.750000 -1.000000 -4.500000
      vertex 3.000000 -1.000000 0.000000
      vertex 28.000000 -1.000000 0.000000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 7.750000 -1.000000 -4.500000
      vertex 28.000000 -1.000000 0.000000
      vertex 9.250000 -1.000000 -4.500000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 7.750000 -1.000000 -6.500000
      vertex 7.750000 -1.000000 -4.500000
      vertex 9.250000 -1.000000 -4.500000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 7.750000 -1.000000 -6.500000
      vertex 9.250000 -1.000000 -4.500000
      vertex 9.250000 -1.000000 -6.000000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 23.250000 -1.000000 -6.500000
      vertex 7.750000 -1.000000 -6.500000
      vertex 9.250000 -1.000000 -6.000000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 23.250000 -1.000000 -6.500000
      vertex 9.250000 -1.000000 -6.000000
      vertex 22.250000 -1.000000 -6.000000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 23.250000 -1.000000 -4.500000
      vertex 23.250000 -1.000000 -6.500000
      vertex 22.250000 -1.000000 -6.000000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 23.250000 -1.000000 -4.500000
      vertex 22.250000 -1.000000 -6.000000
      vertex 22.250000 -1.000000 -4.500000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 28.000000 -1.000000 0.000000
      vertex 23.250000 -1.000000 -4.500000
      vertex 22.250000 -1.000000 -4.500000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 28.000000 -1.000000 0.000000
      vertex 22.250000 -1.000000 -4.500000
      vertex 9.250000 -1.000000 -4.500000
    endloop
  endfacet
  facet normal 0.994138 -0.108118 0.000000
    outer loop
      vertex -1.781296 -0.828024 -9.500000
      vertex -1.800000 -1.000000 -9.500000
      vertex -1.800000 -1.000000 -10.500000
    endloop
  endfacet
  facet normal 0.994138 -0.108118 0.000000
    outer loop
      vertex -1.781296 -0.828024 -9.500000
      vertex -1.800000 -1.000000 -10.500000
      vertex -1.781296 -0.828024 -10.500000
    endloop
  endfacet
  facet normal 0.947653 -0.319302 0.000000
    outer loop
      vertex -1.726060 -0.664089 -9.500000
      vertex -1.781296 -0.828024 -9.500000
      vertex -1.781296 -0.828024 -10.500000
    endloop
  endfacet
  facet normal 0.947653 -0.319302 0.000000
    outer loop
      vertex -1.726060 -0.664089 -9.500000
      vertex -1.781296 -0.828024 -10.500000
      vertex -1.726060 -0.664089 -10.500000
    endloop
  endfacet
  facet normal 0.856857 -0.515554 0.000000
    outer loop
      vertex -1.636874 -0.515861 -9.500000
      vertex -1.726060 -0.664089 -9.500000
      vertex -1.726060 -0.664089 -10.500000
    endloop
  endfacet
  facet normal 0.856857 -0.515554 0.000000
    outer loop
      vertex -1.636874 -0.515861 -9.500000
      vertex -1.726060 -0.664089 -10.500000
      vertex -1.636874 -0.515861 -10.500000
    endloop
  endfacet
  facet normal 0.725996 -0.687699 0.000000
    outer loop
      vertex -1.517909 -0.390270 -9.500000
      vertex -1.636874 -0.515861 -9.500000
      vertex -1.636874 -0.515861 -10.500000
    endloop
  endfacet
  facet normal 0.725996 -0.687699 0.000000
    outer loop
      vertex -1.517909 -0.390270 -9.500000
      vertex -1.636874 -0.515861 -10.500000
      vertex -1.517909 -0.390270 -10.500000
    endloop
  endfacet
  facet normal 0.561187 -0.827689 0.000000
    outer loop
      vertex -1.374727 -0.293190 -9.500000
      vertex -1.517909 -0.390270 -9.500000
      vertex -1.517909 -0.390270 -10.500000
    endloop
  endfacet
  facet normal 0.561187 -0.827689 0.000000
    outer loop
      vertex -1.374727 -0.293190 -9.500000
      vertex -1.517909 -0.390270 -10.500000
      vertex -1.374727 -0.293190 -10.500000
    endloop
  endfacet
  facet normal 0.370138 -0.928977 0.000000
    outer loop
      vertex -1.214023 -0.229160 -9.500000
      vertex -1.374727 -0.293190 -9.500000
      vertex -1.374727 -0.293190 -10.500000
    endloop
  endfacet
  facet normal 0.370138 -0.928977 0.000000
    outer loop
      vertex -1.214023 -0.229160 -9.500000
      vertex -1.374727 -0.293190 -10.500000
      vertex -1.214023 -0.229160 -10.500000
    endloop
  endfacet
  facet normal 0.161782 -0.986827 0.000000
    outer loop
      vertex -1.043311 -0.201173 -9.500000
      vertex -1.214023 -0.229160 -9.500000
      vertex -1.214023 -0.229160 -10.500000
    endloop
  endfacet
  facet normal 0.161782 -0.986827 0.000000
    outer loop
      vertex -1.043311 -0.201173 -9.500000
      vertex -1.214023 -0.229160 -10.500000
      vertex -1.043311 -0.201173 -10.500000
    endloop
  endfacet
  facet normal -0.054139 -0.998533 0.000000
    outer loop
      vertex -0.870574 -0.210539 -9.500000
      vertex -1.043311 -0.201173 -9.500000
      vertex -1.043311 -0.201173 -10.500000
    endloop
  endfacet
  facet normal -0.054139 -0.998533 -0.000000
    outer loop
      vertex -0.870574 -0.210539 -9.500000
      vertex -1.043311 -0.201173 -10.500000
      vertex -0.870574 -0.210539 -10.500000
    endloop
  endfacet
  facet normal -0.267528 -0.963550 0.000000
    outer loop
      vertex -0.703889 -0.256819 -9.500000
      vertex -0.870574 -0.210539 -9.500000
      vertex -0.870574 -0.210539 -10.500000
    endloop
  endfacet
  facet normal -0.267528 -0.963550 -0.000000
    outer loop
      vertex -0.703889 -0.256819 -9.500000
      vertex -0.870574 -0.210539 -10.500000
      vertex -0.703889 -0.256819 -10.500000
    endloop
  endfacet
  facet normal -0.468408 -0.883512 0.000000
    outer loop
      vertex -0.551050 -0.337849 -9.500000
      vertex -0.703889 -0.256819 -9.500000
      vertex -0.703889 -0.256819 -10.500000
    endloop
  endfacet
  facet normal -0.468408 -0.883512 -0.000000
    outer loop
      vertex -0.551050 -0.337849 -9.500000
      vertex -0.703889 -0.256819 -10.500000
      vertex -0.551050 -0.337849 -10.500000
    endloop
  endfacet
  facet normal -0.605174 -0.796093 0.000000
    outer loop
      vertex -0.482091 -0.390270 -9.500000
      vertex -0.551050 -0.337849 -9.500000
      vertex -0.551050 -0.337849 -10.500000
    endloop
  endfacet
  facet normal -0.605174 -0.796093 -0.000000
    outer loop
      vertex -0.482091 -0.390270 -9.500000
      vertex -0.551050 -0.337849 -10.500000
      vertex -0.482091 -0.390270 -10.500000
    endloop
  endfacet
  facet normal -0.725995 -0.687699 0.000000
    outer loop
      vertex -0.363126 -0.515861 -9.500000
      vertex -0.482091 -0.390270 -9.500000
      vertex -0.482091 -0.390270 -10.500000
    endloop
  endfacet
  facet normal -0.725995 -0.687699 -0.000000
    outer loop
      vertex -0.363126 -0.515861 -9.500000
      vertex -0.482091 -0.390270 -10.500000
      vertex -0.363126 -0.515861 -10.500000
    endloop
  endfacet
  facet normal -0.856857 -0.515554 0.000000
    outer loop
      vertex -0.273940 -0.664089 -9.500000
      vertex -0.363126 -0.515861 -9.500000
      vertex -0.363126 -0.515861 -10.500000
    endloop
  endfacet
  facet normal -0.856857 -0.515554 -0.000000
    outer loop
      vertex -0.273940 -0.664089 -9.500000
      vertex -0.363126 -0.515861 -10.500000
      vertex -0.273940 -0.664089 -10.500000
    endloop
  endfacet
  facet normal -0.947653 -0.319302 0.000000
    outer loop
      vertex -0.218704 -0.828024 -9.500000
      vertex -0.273940 -0.664089 -9.500000
      vertex -0.273940 -0.664089 -10.500000
    endloop
  endfacet
  facet normal -0.947653 -0.319302 -0.000000
    outer loop
      vertex -0.218704 -0.828024 -9.500000
      vertex -0.273940 -0.664089 -10.500000
      vertex -0.218704 -0.828024 -10.500000
    endloop
  endfacet
  facet normal -0.994138 -0.108119 0.000000
    outer loop
      vertex -0.200000 -1.000000 -9.500000
      vertex -0.218704 -0.828024 -9.500000
      vertex -0.218704 -0.828024 -10.500000
    endloop
  endfacet
  facet normal -0.994138 -0.108119 -0.000000
    outer loop
      vertex -0.200000 -1.000000 -9.500000
      vertex -0.218704 -0.828024 -10.500000
      vertex -0.200000 -1.000000 -10.500000
    endloop
  endfacet
  facet normal -0.994138 0.108119 0.000000
    outer loop
      vertex -0.218704 -1.171976 -9.500000
      vertex -0.200000 -1.000000 -9.500000
      vertex -0.200000 -1.000000 -10.500000
    endloop
  endfacet
  facet normal -0.994138 0.108119 0.000000
    outer loop
      vertex -0.218704 -1.171976 -9.500000
      vertex -0.200000 -1.000000 -10.500000
      vertex -0.218704 -1.171976 -10.500000
    endloop
  endfacet
  facet normal -0.947653 0.319301 0.000000
    outer loop
      vertex -0.273940 -1.335911 -9.500000
      vertex -0.218704 -1.171976 -9.500000
      vertex -0.218704 -1.171976 -10.500000
    endloop
  endfacet
  facet normal -0.947653 0.319301 0.000000
    outer loop
      vertex -0.273940 -1.335911 -9.500000
      vertex -0.218704 -1.171976 -10.500000
      vertex -0.273940 -1.335911 -10.500000
    endloop
  endfacet
  facet normal -0.856857 0.515554 0.000000
    outer loop
      vertex -0.363126 -1.484139 -9.500000
      vertex -0.273940 -1.335911 -9.500000
      vertex -0.273940 -1.335911 -10.500000
    endloop
  endfacet
  facet normal -0.856857 0.515554 0.000000
    outer loop
      vertex -0.363126 -1.484139 -9.500000
      vertex -0.273940 -1.335911 -10.500000
      vertex -0.363126 -1.484139 -10.500000
    endloop
  endfacet
  facet normal -0.725996 0.687699 0.000000
    outer loop
      vertex -0.482091 -1.609730 -9.500000
      vertex -0.363126 -1.484139 -9.500000
      vertex -0.363126 -1.484139 -10.500000
    endloop
  endfacet
  facet normal -0.725996 0.687699 0.000000
    outer loop
      vertex -0.482091 -1.609730 -9.500000
      vertex -0.363126 -1.484139 -10.500000
      vertex -0.482091 -1.609730 -10.500000
    endloop
  endfacet
  facet normal -0.605174 0.796093 0.000000
    outer loop
      vertex -0.551050 -1.662151 -9.500000
      vertex -0.482091 -1.609730 -9.500000
      vertex -0.482091 -1.609730 -10.500000
    endloop
  endfacet
  facet normal -0.605174 0.796093 0.000000
    outer loop
      vertex -0.551050 -1.662151 -9.500000
      vertex -0.482091 -1.609730 -10.500000
      vertex -0.551050 -1.662151 -10.500000
    endloop
  endfacet
  facet normal -0.515554 0.856857 0.000000
    outer loop
      vertex -0.625273 -1.706810 -9.500000
      vertex -0.551050 -1.662151 -9.500000
      vertex -0.551050 -1.662151 -10.500000
    endloop
  endfacet
  facet normal -0.515554 0.856857 0.000000
    outer loop
      vertex -0.625273 -1.706810 -9.500000
      vertex -0.551050 -1.662151 -10.500000
      vertex -0.625273 -1.706810 -10.500000
    endloop
  endfacet
  facet normal -0.370138 0.928977 0.000000
    outer loop
      vertex -0.785977 -1.770840 -9.500000
      vertex -0.625273 -1.706810 -9.500000
      vertex -0.625273 -1.706810 -10.500000
    endloop
  endfacet
  facet normal -0.370138 0.928977 0.000000
    outer loop
      vertex -0.785977 -1.770840 -9.500000
      vertex -0.625273 -1.706810 -10.500000
      vertex -0.785977 -1.770840 -10.500000
    endloop
  endfacet
  facet normal -0.161782 0.986827 0.000000
    outer loop
      vertex -0.956689 -1.798827 -9.500000
      vertex -0.785977 -1.770840 -9.500000
      vertex -0.785977 -1.770840 -10.500000
    endloop
  endfacet
  facet normal -0.161782 0.986827 0.000000
    outer loop
      vertex -0.956689 -1.798827 -9.500000
      vertex -0.785977 -1.770840 -10.500000
      vertex -0.956689 -1.798827 -10.500000
    endloop
  endfacet
  facet normal 0.054138 0.998533 0.000000
    outer loop
      vertex -1.129426 -1.789461 -9.500000
      vertex -0.956689 -1.798827 -9.500000
      vertex -0.956689 -1.798827 -10.500000
    endloop
  endfacet
  facet normal 0.054138 0.998533 0.000000
    outer loop
      vertex -1.129426 -1.789461 -9.500000
      vertex -0.956689 -1.798827 -10.500000
      vertex -1.129426 -1.789461 -10.500000
    endloop
  endfacet
  facet normal 0.267529 0.963550 0.000000
    outer loop
      vertex -1.296111 -1.743181 -9.500000
      vertex -1.129426 -1.789461 -9.500000
      vertex -1.129426 -1.789461 -10.500000
    endloop
  endfacet
  facet normal 0.267529 0.963550 0.000000
    outer loop
      vertex -1.296111 -1.743181 -9.500000
      vertex -1.129426 -1.789461 -10.500000
      vertex -1.296111 -1.743181 -10.500000
    endloop
  endfacet
  facet normal 0.468408 0.883512 0.000000
    outer loop
      vertex -1.448950 -1.662151 -9.500000
      vertex -1.296111 -1.743181 -9.500000
      vertex -1.296111 -1.743181 -10.500000
    endloop
  endfacet
  facet normal 0.468408 0.883512 0.000000
    outer loop
      vertex -1.448950 -1.662151 -9.500000
      vertex -1.296111 -1.743181 -10.500000
      vertex -1.448950 -1.662151 -10.500000
    endloop
  endfacet
  facet normal 0.647386 0.762162 0.000000
    outer loop
      vertex -1.580796 -1.550160 -9.500000
      vertex -1.448950 -1.662151 -9.500000
      vertex -1.448950 -1.662151 -10.500000
    endloop
  endfacet
  facet normal 0.647386 0.762162 0.000000
    outer loop
      vertex -1.580796 -1.550160 -9.500000
      vertex -1.448950 -1.662151 -10.500000
      vertex -1.580796 -1.550160 -10.500000
    endloop
  endfacet
  facet normal 0.796093 0.605174 0.000000
    outer loop
      vertex -1.685486 -1.412443 -9.500000
      vertex -1.580796 -1.550160 -9.500000
      vertex -1.580796 -1.550160 -10.500000
    endloop
  endfacet
  facet normal 0.796093 0.605174 0.000000
    outer loop
      vertex -1.685486 -1.412443 -9.500000
      vertex -1.580796 -1.550160 -10.500000
      vertex -1.685486 -1.412443 -10.500000
    endloop
  endfacet
  facet normal 0.907575 0.419889 0.000000
    outer loop
      vertex -1.758123 -1.255441 -9.500000
      vertex -1.685486 -1.412443 -9.500000
      vertex -1.685486 -1.412443 -10.500000
    endloop
  endfacet
  facet normal 0.907575 0.419889 0.000000
    outer loop
      vertex -1.758123 -1.255441 -9.500000
      vertex -1.685486 -1.412443 -10.500000
      vertex -1.758123 -1.255441 -10.500000
    endloop
  endfacet
  facet normal 0.976621 0.214970 0.000000
    outer loop
      vertex -1.795310 -1.086495 -9.500000
      vertex -1.758123 -1.255441 -9.500000
      vertex -1.758123 -1.255441 -10.500000
    endloop
  endfacet
  facet normal 0.976621 0.214970 0.000000
    outer loop
      vertex -1.795310 -1.086495 -9.500000
      vertex -1.758123 -1.255441 -10.500000
      vertex -1.795310 -1.086495 -10.500000
    endloop
  endfacet
  facet normal 0.998533 0.054138 0.000000
    outer loop
      vertex -1.800000 -1.000000 -9.500000
      vertex -1.795310 -1.086495 -9.500000
      vertex -1.795310 -1.086495 -10.500000
    endloop
  endfacet
  facet normal 0.998533 0.054138 0.000000
    outer loop
      vertex -1.800000 -1.000000 -9.500000
      vertex -1.795310 -1.086495 -10.500000
      vertex -1.800000 -1.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex -0.100000 74.000000 -10.500000
      vertex -1.000000 74.000000 -10.500000
      vertex -1.000000 74.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 1.000000 -0.000000
    outer loop
      vertex -0.100000 74.000000 -10.500000
      vertex -1.000000 74.000000 23.000000
      vertex -0.100000 74.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 32.000000 74.000000 -10.500000
      vertex -0.100000 74.000000 -10.500000
      vertex -0.100000 74.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 1.000000 -0.000000
    outer loop
      vertex 32.000000 74.000000 -10.500000
      vertex -0.100000 74.000000 23.000000
      vertex 32.000000 74.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 -1.000000 -9.500000
      vertex -1.800000 -1.000000 -9.500000
      vertex -1.781296 -0.828024 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 -1.000000 -9.500000
      vertex -1.685486 -1.412443 -9.500000
      vertex -1.758123 -1.255441 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 -1.000000 -9.500000
      vertex -1.758123 -1.255441 -9.500000
      vertex -1.795310 -1.086495 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.800000 -1.000000 -9.500000
      vertex -1.000000 -1.000000 -9.500000
      vertex -1.795310 -1.086495 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 -1.000000 -9.500000
      vertex -1.296111 -1.743181 -9.500000
      vertex -1.448950 -1.662151 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 -1.000000 -9.500000
      vertex -1.448950 -1.662151 -9.500000
      vertex -1.580796 -1.550160 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.685486 -1.412443 -9.500000
      vertex -1.000000 -1.000000 -9.500000
      vertex -1.580796 -1.550160 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 -1.000000 -9.500000
      vertex -0.785977 -1.770840 -9.500000
      vertex -0.956689 -1.798827 -9.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex -1.000000 -1.000000 -9.500000
      vertex -0.956689 -1.798827 -9.500000
      vertex -1.129426 -1.789461 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.296111 -1.743181 -9.500000
      vertex -1.000000 -1.000000 -9.500000
      vertex -1.129426 -1.789461 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 -1.000000 -9.500000
      vertex -0.482091 -1.609730 -9.500000
      vertex -0.551050 -1.662151 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 -1.000000 -9.500000
      vertex -0.551050 -1.662151 -9.500000
      vertex -0.625273 -1.706810 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.785977 -1.770840 -9.500000
      vertex -1.000000 -1.000000 -9.500000
      vertex -0.625273 -1.706810 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 -1.000000 -9.500000
      vertex -0.218704 -1.171976 -9.500000
      vertex -0.273940 -1.335911 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 -1.000000 -9.500000
      vertex -0.273940 -1.335911 -9.500000
      vertex -0.363126 -1.484139 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.482091 -1.609730 -9.500000
      vertex -1.000000 -1.000000 -9.500000
      vertex -0.363126 -1.484139 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 -1.000000 -9.500000
      vertex -0.273940 -0.664089 -9.500000
      vertex -0.218704 -0.828024 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 -1.000000 -9.500000
      vertex -0.218704 -0.828024 -9.500000
      vertex -0.200000 -1.000000 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -0.218704 -1.171976 -9.500000
      vertex -1.000000 -1.000000 -9.500000
      vertex -0.200000 -1.000000 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 -1.000000 -9.500000
      vertex -0.551050 -0.337849 -9.500000
      vertex -0.482091 -0.390270 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 -1.000000 -9.500000
      vertex -0.482091 -0.390270 -9.500000
      vertex -0.363126 -0.515861 -9.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex -0.273940 -0.664089 -9.500000
      vertex -1.000000 -1.000000 -9.500000
      vertex -0.363126 -0.515861 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 -1.000000 -9.500000
      vertex -1.043311 -0.201173 -9.500000
      vertex -0.870574 -0.210539 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 -1.000000 -9.500000
      vertex -0.870574 -0.210539 -9.500000
      vertex -0.703889 -0.256819 -9.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex -0.551050 -0.337849 -9.500000
      vertex -1.000000 -1.000000 -9.500000
      vertex -0.703889 -0.256819 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 -1.000000 -9.500000
      vertex -1.517909 -0.390270 -9.500000
      vertex -1.374727 -0.293190 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 -1.000000 -9.500000
      vertex -1.374727 -0.293190 -9.500000
      vertex -1.214023 -0.229160 -9.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex -1.043311 -0.201173 -9.500000
      vertex -1.000000 -1.000000 -9.500000
      vertex -1.214023 -0.229160 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 -1.000000 -9.500000
      vertex -1.781296 -0.828024 -9.500000
      vertex -1.726060 -0.664089 -9.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex -1.000000 -1.000000 -9.500000
      vertex -1.726060 -0.664089 -9.500000
      vertex -1.636874 -0.515861 -9.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex -1.517909 -0.390270 -9.500000
      vertex -1.000000 -1.000000 -9.500000
      vertex -1.636874 -0.515861 -9.500000
    endloop
  endfacet
  facet normal 1.000000 0.000000 -0.000000
    outer loop
      vertex 3.000000 0.000000 -4.500000
      vertex 3.000000 0.000000 0.000000
      vertex 3.000000 -1.000000 0.000000
    endloop
  endfacet
  facet normal 1.000000 0.000000 0.000000
    outer loop
      vertex 3.000000 0.000000 -4.500000
      vertex 3.000000 -1.000000 0.000000
      vertex 3.000000 -1.000000 -4.500000
    endloop
  endfacet
  facet normal -0.994138 -0.108116 0.000000
    outer loop
      vertex -0.218704 72.171982 22.000000
      vertex -0.200000 72.000000 22.000000
      vertex -0.200000 72.000000 23.000000
    endloop
  endfacet
  facet normal -0.994138 -0.108116 0.000000
    outer loop
      vertex -0.218704 72.171982 22.000000
      vertex -0.200000 72.000000 23.000000
      vertex -0.218704 72.171982 23.000000
    endloop
  endfacet
  facet normal -0.947652 -0.319305 0.000000
    outer loop
      vertex -0.273940 72.335915 22.000000
      vertex -0.218704 72.171982 22.000000
      vertex -0.218704 72.171982 23.000000
    endloop
  endfacet
  facet normal -0.947652 -0.319305 0.000000
    outer loop
      vertex -0.273940 72.335915 22.000000
      vertex -0.218704 72.171982 23.000000
      vertex -0.273940 72.335915 23.000000
    endloop
  endfacet
  facet normal -0.856862 -0.515545 0.000000
    outer loop
      vertex -0.363126 72.484146 22.000000
      vertex -0.273940 72.335915 22.000000
      vertex -0.273940 72.335915 23.000000
    endloop
  endfacet
  facet normal -0.856862 -0.515545 0.000000
    outer loop
      vertex -0.363126 72.484146 22.000000
      vertex -0.273940 72.335915 23.000000
      vertex -0.363126 72.484146 23.000000
    endloop
  endfacet
  facet normal -0.725988 -0.687708 0.000000
    outer loop
      vertex -0.482091 72.609734 22.000000
      vertex -0.363126 72.484146 22.000000
      vertex -0.363126 72.484146 23.000000
    endloop
  endfacet
  facet normal -0.725988 -0.687708 0.000000
    outer loop
      vertex -0.482091 72.609734 22.000000
      vertex -0.363126 72.484146 23.000000
      vertex -0.482091 72.609734 23.000000
    endloop
  endfacet
  facet normal -0.561173 -0.827699 0.000000
    outer loop
      vertex -0.625273 72.706810 22.000000
      vertex -0.482091 72.609734 22.000000
      vertex -0.482091 72.609734 23.000000
    endloop
  endfacet
  facet normal -0.561173 -0.827699 0.000000
    outer loop
      vertex -0.625273 72.706810 22.000000
      vertex -0.482091 72.609734 23.000000
      vertex -0.625273 72.706810 23.000000
    endloop
  endfacet
  facet normal -0.370154 -0.928970 0.000000
    outer loop
      vertex -0.785977 72.770844 22.000000
      vertex -0.625273 72.706810 22.000000
      vertex -0.625273 72.706810 23.000000
    endloop
  endfacet
  facet normal -0.370154 -0.928970 0.000000
    outer loop
      vertex -0.785977 72.770844 22.000000
      vertex -0.625273 72.706810 23.000000
      vertex -0.785977 72.770844 23.000000
    endloop
  endfacet
  facet normal -0.161770 -0.986828 0.000000
    outer loop
      vertex -0.956689 72.798828 22.000000
      vertex -0.785977 72.770844 22.000000
      vertex -0.785977 72.770844 23.000000
    endloop
  endfacet
  facet normal -0.161770 -0.986828 0.000000
    outer loop
      vertex -0.956689 72.798828 22.000000
      vertex -0.785977 72.770844 23.000000
      vertex -0.956689 72.798828 23.000000
    endloop
  endfacet
  facet normal 0.054158 -0.998532 0.000000
    outer loop
      vertex -1.129426 72.789459 22.000000
      vertex -0.956689 72.798828 22.000000
      vertex -0.956689 72.798828 23.000000
    endloop
  endfacet
  facet normal 0.054158 -0.998532 0.000000
    outer loop
      vertex -1.129426 72.789459 22.000000
      vertex -0.956689 72.798828 23.000000
      vertex -1.129426 72.789459 23.000000
    endloop
  endfacet
  facet normal 0.267488 -0.963561 0.000000
    outer loop
      vertex -1.296111 72.743187 22.000000
      vertex -1.129426 72.789459 22.000000
      vertex -1.129426 72.789459 23.000000
    endloop
  endfacet
  facet normal 0.267488 -0.963561 0.000000
    outer loop
      vertex -1.296111 72.743187 22.000000
      vertex -1.129426 72.789459 23.000000
      vertex -1.296111 72.743187 23.000000
    endloop
  endfacet
  facet normal 0.468416 -0.883508 0.000000
    outer loop
      vertex -1.448950 72.662155 22.000000
      vertex -1.296111 72.743187 22.000000
      vertex -1.296111 72.743187 23.000000
    endloop
  endfacet
  facet normal 0.468416 -0.883508 0.000000
    outer loop
      vertex -1.448950 72.662155 22.000000
      vertex -1.296111 72.743187 23.000000
      vertex -1.448950 72.662155 23.000000
    endloop
  endfacet
  facet normal 0.605174 -0.796093 0.000000
    outer loop
      vertex -1.517909 72.609734 22.000000
      vertex -1.448950 72.662155 22.000000
      vertex -1.448950 72.662155 23.000000
    endloop
  endfacet
  facet normal 0.605174 -0.796093 0.000000
    outer loop
      vertex -1.517909 72.609734 22.000000
      vertex -1.448950 72.662155 23.000000
      vertex -1.517909 72.609734 23.000000
    endloop
  endfacet
  facet normal 0.725988 -0.687707 0.000000
    outer loop
      vertex -1.636874 72.484146 22.000000
      vertex -1.517909 72.609734 22.000000
      vertex -1.517909 72.609734 23.000000
    endloop
  endfacet
  facet normal 0.725988 -0.687707 0.000000
    outer loop
      vertex -1.636874 72.484146 22.000000
      vertex -1.517909 72.609734 23.000000
      vertex -1.636874 72.484146 23.000000
    endloop
  endfacet
  facet normal 0.856863 -0.515545 0.000000
    outer loop
      vertex -1.726060 72.335915 22.000000
      vertex -1.636874 72.484146 22.000000
      vertex -1.636874 72.484146 23.000000
    endloop
  endfacet
  facet normal 0.856863 -0.515545 0.000000
    outer loop
      vertex -1.726060 72.335915 22.000000
      vertex -1.636874 72.484146 23.000000
      vertex -1.726060 72.335915 23.000000
    endloop
  endfacet
  facet normal 0.947652 -0.319306 0.000000
    outer loop
      vertex -1.781296 72.171982 22.000000
      vertex -1.726060 72.335915 22.000000
      vertex -1.726060 72.335915 23.000000
    endloop
  endfacet
  facet normal 0.947652 -0.319306 0.000000
    outer loop
      vertex -1.781296 72.171982 22.000000
      vertex -1.726060 72.335915 23.000000
      vertex -1.781296 72.171982 23.000000
    endloop
  endfacet
  facet normal 0.994138 -0.108115 0.000000
    outer loop
      vertex -1.800000 72.000000 22.000000
      vertex -1.781296 72.171982 22.000000
      vertex -1.781296 72.171982 23.000000
    endloop
  endfacet
  facet normal 0.994138 -0.108115 0.000000
    outer loop
      vertex -1.800000 72.000000 22.000000
      vertex -1.781296 72.171982 23.000000
      vertex -1.800000 72.000000 23.000000
    endloop
  endfacet
  facet normal 0.994138 0.108120 0.000000
    outer loop
      vertex -1.781296 71.828026 22.000000
      vertex -1.800000 72.000000 22.000000
      vertex -1.800000 72.000000 23.000000
    endloop
  endfacet
  facet normal 0.994138 0.108120 -0.000000
    outer loop
      vertex -1.781296 71.828026 22.000000
      vertex -1.800000 72.000000 23.000000
      vertex -1.781296 71.828026 23.000000
    endloop
  endfacet
  facet normal 0.947656 0.319292 0.000000
    outer loop
      vertex -1.726060 71.664085 22.000000
      vertex -1.781296 71.828026 22.000000
      vertex -1.781296 71.828026 23.000000
    endloop
  endfacet
  facet normal 0.947656 0.319292 -0.000000
    outer loop
      vertex -1.726060 71.664085 22.000000
      vertex -1.781296 71.828026 23.000000
      vertex -1.726060 71.664085 23.000000
    endloop
  endfacet
  facet normal 0.856851 0.515564 0.000000
    outer loop
      vertex -1.636874 71.515862 22.000000
      vertex -1.726060 71.664085 22.000000
      vertex -1.726060 71.664085 23.000000
    endloop
  endfacet
  facet normal 0.856851 0.515564 -0.000000
    outer loop
      vertex -1.636874 71.515862 22.000000
      vertex -1.726060 71.664085 23.000000
      vertex -1.636874 71.515862 23.000000
    endloop
  endfacet
  facet normal 0.725988 0.687707 0.000000
    outer loop
      vertex -1.517909 71.390274 22.000000
      vertex -1.636874 71.515862 22.000000
      vertex -1.636874 71.515862 23.000000
    endloop
  endfacet
  facet normal 0.725988 0.687707 -0.000000
    outer loop
      vertex -1.517909 71.390274 22.000000
      vertex -1.636874 71.515862 23.000000
      vertex -1.517909 71.390274 23.000000
    endloop
  endfacet
  facet normal 0.605174 0.796093 0.000000
    outer loop
      vertex -1.448950 71.337852 22.000000
      vertex -1.517909 71.390274 22.000000
      vertex -1.517909 71.390274 23.000000
    endloop
  endfacet
  facet normal 0.605174 0.796093 -0.000000
    outer loop
      vertex -1.448950 71.337852 22.000000
      vertex -1.517909 71.390274 23.000000
      vertex -1.448950 71.337852 23.000000
    endloop
  endfacet
  facet normal 0.515588 0.856837 0.000000
    outer loop
      vertex -1.374727 71.293190 22.000000
      vertex -1.448950 71.337852 22.000000
      vertex -1.448950 71.337852 23.000000
    endloop
  endfacet
  facet normal 0.515588 0.856837 -0.000000
    outer loop
      vertex -1.374727 71.293190 22.000000
      vertex -1.448950 71.337852 23.000000
      vertex -1.374727 71.293190 23.000000
    endloop
  endfacet
  facet normal 0.370154 0.928971 0.000000
    outer loop
      vertex -1.214023 71.229156 22.000000
      vertex -1.374727 71.293190 22.000000
      vertex -1.374727 71.293190 23.000000
    endloop
  endfacet
  facet normal 0.370154 0.928971 -0.000000
    outer loop
      vertex -1.214023 71.229156 22.000000
      vertex -1.374727 71.293190 23.000000
      vertex -1.214023 71.229156 23.000000
    endloop
  endfacet
  facet normal 0.161770 0.986828 0.000000
    outer loop
      vertex -1.043311 71.201172 22.000000
      vertex -1.214023 71.229156 22.000000
      vertex -1.214023 71.229156 23.000000
    endloop
  endfacet
  facet normal 0.161770 0.986828 -0.000000
    outer loop
      vertex -1.043311 71.201172 22.000000
      vertex -1.214023 71.229156 23.000000
      vertex -1.043311 71.201172 23.000000
    endloop
  endfacet
  facet normal -0.054158 0.998532 0.000000
    outer loop
      vertex -0.870574 71.210541 22.000000
      vertex -1.043311 71.201172 22.000000
      vertex -1.043311 71.201172 23.000000
    endloop
  endfacet
  facet normal -0.054158 0.998532 0.000000
    outer loop
      vertex -0.870574 71.210541 22.000000
      vertex -1.043311 71.201172 23.000000
      vertex -0.870574 71.210541 23.000000
    endloop
  endfacet
  facet normal -0.267488 0.963561 0.000000
    outer loop
      vertex -0.703889 71.256813 22.000000
      vertex -0.870574 71.210541 22.000000
      vertex -0.870574 71.210541 23.000000
    endloop
  endfacet
  facet normal -0.267488 0.963561 0.000000
    outer loop
      vertex -0.703889 71.256813 22.000000
      vertex -0.870574 71.210541 23.000000
      vertex -0.703889 71.256813 23.000000
    endloop
  endfacet
  facet normal -0.468450 0.883490 0.000000
    outer loop
      vertex -0.551050 71.337852 22.000000
      vertex -0.703889 71.256813 22.000000
      vertex -0.703889 71.256813 23.000000
    endloop
  endfacet
  facet normal -0.468450 0.883490 0.000000
    outer loop
      vertex -0.551050 71.337852 22.000000
      vertex -0.703889 71.256813 23.000000
      vertex -0.551050 71.337852 23.000000
    endloop
  endfacet
  facet normal -0.647362 0.762183 0.000000
    outer loop
      vertex -0.419204 71.449837 22.000000
      vertex -0.551050 71.337852 22.000000
      vertex -0.551050 71.337852 23.000000
    endloop
  endfacet
  facet normal -0.647362 0.762183 0.000000
    outer loop
      vertex -0.419204 71.449837 22.000000
      vertex -0.551050 71.337852 23.000000
      vertex -0.419204 71.449837 23.000000
    endloop
  endfacet
  facet normal -0.796097 0.605169 0.000000
    outer loop
      vertex -0.314514 71.587555 22.000000
      vertex -0.419204 71.449837 22.000000
      vertex -0.419204 71.449837 23.000000
    endloop
  endfacet
  facet normal -0.796097 0.605169 0.000000
    outer loop
      vertex -0.314514 71.587555 22.000000
      vertex -0.419204 71.449837 23.000000
      vertex -0.314514 71.587555 23.000000
    endloop
  endfacet
  facet normal -0.907579 0.419882 0.000000
    outer loop
      vertex -0.241877 71.744560 22.000000
      vertex -0.314514 71.587555 22.000000
      vertex -0.314514 71.587555 23.000000
    endloop
  endfacet
  facet normal -0.907579 0.419882 0.000000
    outer loop
      vertex -0.241877 71.744560 22.000000
      vertex -0.314514 71.587555 23.000000
      vertex -0.241877 71.744560 23.000000
    endloop
  endfacet
  facet normal -0.976620 0.214971 0.000000
    outer loop
      vertex -0.204690 71.913506 22.000000
      vertex -0.241877 71.744560 22.000000
      vertex -0.241877 71.744560 23.000000
    endloop
  endfacet
  facet normal -0.976620 0.214971 0.000000
    outer loop
      vertex -0.204690 71.913506 22.000000
      vertex -0.241877 71.744560 23.000000
      vertex -0.204690 71.913506 23.000000
    endloop
  endfacet
  facet normal -0.998533 0.054140 0.000000
    outer loop
      vertex -0.200000 72.000000 22.000000
      vertex -0.204690 71.913506 22.000000
      vertex -0.204690 71.913506 23.000000
    endloop
  endfacet
  facet normal -0.998533 0.054140 0.000000
    outer loop
      vertex -0.200000 72.000000 22.000000
      vertex -0.204690 71.913506 23.000000
      vertex -0.200000 72.000000 23.000000
    endloop
  endfacet
  facet normal 1.000000 0.000000 0.000000
    outer loop
      vertex 28.000000 0.000000 -4.500000
      vertex 28.000000 0.000000 -6.500000
      vertex 28.000000 3.000000 -6.500000
    endloop
  endfacet
  facet normal 1.000000 -0.000000 0.000000
    outer loop
      vertex 28.000000 0.000000 -4.500000
      vertex 28.000000 3.000000 -6.500000
      vertex 28.000000 3.000000 -4.500000
    endloop
  endfacet
  facet normal -0.994138 -0.108115 0.000000
    outer loop
      vertex 32.781296 72.171982 22.000000
      vertex 32.799999 72.000000 22.000000
      vertex 32.799999 72.000000 23.000000
    endloop
  endfacet
  facet normal -0.994138 -0.108115 0.000000
    outer loop
      vertex 32.781296 72.171982 22.000000
      vertex 32.799999 72.000000 23.000000
      vertex 32.781296 72.171982 23.000000
    endloop
  endfacet
  facet normal -0.947651 -0.319309 0.000000
    outer loop
      vertex 32.726059 72.335915 22.000000
      vertex 32.781296 72.171982 22.000000
      vertex 32.781296 72.171982 23.000000
    endloop
  endfacet
  facet normal -0.947651 -0.319309 0.000000
    outer loop
      vertex 32.726059 72.335915 22.000000
      vertex 32.781296 72.171982 23.000000
      vertex 32.726059 72.335915 23.000000
    endloop
  endfacet
  facet normal -0.856868 -0.515536 0.000000
    outer loop
      vertex 32.636875 72.484146 22.000000
      vertex 32.726059 72.335915 22.000000
      vertex 32.726059 72.335915 23.000000
    endloop
  endfacet
  facet normal -0.856868 -0.515536 0.000000
    outer loop
      vertex 32.636875 72.484146 22.000000
      vertex 32.726059 72.335915 23.000000
      vertex 32.636875 72.484146 23.000000
    endloop
  endfacet
  facet normal -0.725989 -0.687707 0.000000
    outer loop
      vertex 32.517910 72.609734 22.000000
      vertex 32.636875 72.484146 22.000000
      vertex 32.636875 72.484146 23.000000
    endloop
  endfacet
  facet normal -0.725989 -0.687707 0.000000
    outer loop
      vertex 32.517910 72.609734 22.000000
      vertex 32.636875 72.484146 23.000000
      vertex 32.517910 72.609734 23.000000
    endloop
  endfacet
  facet normal -0.561177 -0.827696 0.000000
    outer loop
      vertex 32.374729 72.706810 22.000000
      vertex 32.517910 72.609734 22.000000
      vertex 32.517910 72.609734 23.000000
    endloop
  endfacet
  facet normal -0.561177 -0.827696 0.000000
    outer loop
      vertex 32.374729 72.706810 22.000000
      vertex 32.517910 72.609734 23.000000
      vertex 32.374729 72.706810 23.000000
    endloop
  endfacet
  facet normal -0.370151 -0.928972 0.000000
    outer loop
      vertex 32.214024 72.770844 22.000000
      vertex 32.374729 72.706810 22.000000
      vertex 32.374729 72.706810 23.000000
    endloop
  endfacet
  facet normal -0.370151 -0.928972 0.000000
    outer loop
      vertex 32.214024 72.770844 22.000000
      vertex 32.374729 72.706810 23.000000
      vertex 32.214024 72.770844 23.000000
    endloop
  endfacet
  facet normal -0.161770 -0.986828 0.000000
    outer loop
      vertex 32.043312 72.798828 22.000000
      vertex 32.214024 72.770844 22.000000
      vertex 32.214024 72.770844 23.000000
    endloop
  endfacet
  facet normal -0.161770 -0.986828 0.000000
    outer loop
      vertex 32.043312 72.798828 22.000000
      vertex 32.214024 72.770844 23.000000
      vertex 32.043312 72.798828 23.000000
    endloop
  endfacet
  facet normal 0.054158 -0.998532 0.000000
    outer loop
      vertex 31.870573 72.789459 22.000000
      vertex 32.043312 72.798828 22.000000
      vertex 32.043312 72.798828 23.000000
    endloop
  endfacet
  facet normal 0.054158 -0.998532 0.000000
    outer loop
      vertex 31.870573 72.789459 22.000000
      vertex 32.043312 72.798828 23.000000
      vertex 31.870573 72.789459 23.000000
    endloop
  endfacet
  facet normal 0.267490 -0.963561 0.000000
    outer loop
      vertex 31.703890 72.743187 22.000000
      vertex 31.870573 72.789459 22.000000
      vertex 31.870573 72.789459 23.000000
    endloop
  endfacet
  facet normal 0.267490 -0.963561 0.000000
    outer loop
      vertex 31.703890 72.743187 22.000000
      vertex 31.870573 72.789459 23.000000
      vertex 31.703890 72.743187 23.000000
    endloop
  endfacet
  facet normal 0.468419 -0.883506 0.000000
    outer loop
      vertex 31.551052 72.662155 22.000000
      vertex 31.703890 72.743187 22.000000
      vertex 31.703890 72.743187 23.000000
    endloop
  endfacet
  facet normal 0.468419 -0.883506 0.000000
    outer loop
      vertex 31.551052 72.662155 22.000000
      vertex 31.703890 72.743187 23.000000
      vertex 31.551052 72.662155 23.000000
    endloop
  endfacet
  facet normal 0.605159 -0.796104 0.000000
    outer loop
      vertex 31.482090 72.609734 22.000000
      vertex 31.551052 72.662155 22.000000
      vertex 31.551052 72.662155 23.000000
    endloop
  endfacet
  facet normal 0.605159 -0.796104 0.000000
    outer loop
      vertex 31.482090 72.609734 22.000000
      vertex 31.551052 72.662155 23.000000
      vertex 31.482090 72.609734 23.000000
    endloop
  endfacet
  facet normal 0.725994 -0.687701 0.000000
    outer loop
      vertex 31.363127 72.484146 22.000000
      vertex 31.482090 72.609734 22.000000
      vertex 31.482090 72.609734 23.000000
    endloop
  endfacet
  facet normal 0.725994 -0.687701 0.000000
    outer loop
      vertex 31.363127 72.484146 22.000000
      vertex 31.482090 72.609734 23.000000
      vertex 31.363127 72.484146 23.000000
    endloop
  endfacet
  facet normal 0.856858 -0.515553 0.000000
    outer loop
      vertex 31.273939 72.335915 22.000000
      vertex 31.363127 72.484146 22.000000
      vertex 31.363127 72.484146 23.000000
    endloop
  endfacet
  facet normal 0.856858 -0.515553 0.000000
    outer loop
      vertex 31.273939 72.335915 22.000000
      vertex 31.363127 72.484146 23.000000
      vertex 31.273939 72.335915 23.000000
    endloop
  endfacet
  facet normal 0.947654 -0.319299 0.000000
    outer loop
      vertex 31.218704 72.171982 22.000000
      vertex 31.273939 72.335915 22.000000
      vertex 31.273939 72.335915 23.000000
    endloop
  endfacet
  facet normal 0.947654 -0.319299 0.000000
    outer loop
      vertex 31.218704 72.171982 22.000000
      vertex 31.273939 72.335915 23.000000
      vertex 31.218704 72.171982 23.000000
    endloop
  endfacet
  facet normal 0.994137 -0.108126 0.000000
    outer loop
      vertex 31.199999 72.000000 22.000000
      vertex 31.218704 72.171982 22.000000
      vertex 31.218704 72.171982 23.000000
    endloop
  endfacet
  facet normal 0.994137 -0.108126 0.000000
    outer loop
      vertex 31.199999 72.000000 22.000000
      vertex 31.218704 72.171982 23.000000
      vertex 31.199999 72.000000 23.000000
    endloop
  endfacet
  facet normal 0.994137 0.108131 0.000000
    outer loop
      vertex 31.218704 71.828026 22.000000
      vertex 31.199999 72.000000 22.000000
      vertex 31.199999 72.000000 23.000000
    endloop
  endfacet
  facet normal 0.994137 0.108131 -0.000000
    outer loop
      vertex 31.218704 71.828026 22.000000
      vertex 31.199999 72.000000 23.000000
      vertex 31.218704 71.828026 23.000000
    endloop
  endfacet
  facet normal 0.947659 0.319286 0.000000
    outer loop
      vertex 31.273939 71.664085 22.000000
      vertex 31.218704 71.828026 22.000000
      vertex 31.218704 71.828026 23.000000
    endloop
  endfacet
  facet normal 0.947659 0.319286 -0.000000
    outer loop
      vertex 31.273939 71.664085 22.000000
      vertex 31.218704 71.828026 23.000000
      vertex 31.273939 71.664085 23.000000
    endloop
  endfacet
  facet normal 0.856846 0.515572 0.000000
    outer loop
      vertex 31.363127 71.515862 22.000000
      vertex 31.273939 71.664085 22.000000
      vertex 31.273939 71.664085 23.000000
    endloop
  endfacet
  facet normal 0.856846 0.515572 -0.000000
    outer loop
      vertex 31.363127 71.515862 22.000000
      vertex 31.273939 71.664085 23.000000
      vertex 31.363127 71.515862 23.000000
    endloop
  endfacet
  facet normal 0.725994 0.687701 0.000000
    outer loop
      vertex 31.482090 71.390274 22.000000
      vertex 31.363127 71.515862 22.000000
      vertex 31.363127 71.515862 23.000000
    endloop
  endfacet
  facet normal 0.725994 0.687701 -0.000000
    outer loop
      vertex 31.482090 71.390274 22.000000
      vertex 31.363127 71.515862 23.000000
      vertex 31.482090 71.390274 23.000000
    endloop
  endfacet
  facet normal 0.605159 0.796104 0.000000
    outer loop
      vertex 31.551052 71.337852 22.000000
      vertex 31.482090 71.390274 22.000000
      vertex 31.482090 71.390274 23.000000
    endloop
  endfacet
  facet normal 0.605159 0.796104 -0.000000
    outer loop
      vertex 31.551052 71.337852 22.000000
      vertex 31.482090 71.390274 23.000000
      vertex 31.551052 71.337852 23.000000
    endloop
  endfacet
  facet normal 0.515590 0.856836 0.000000
    outer loop
      vertex 31.625275 71.293190 22.000000
      vertex 31.551052 71.337852 22.000000
      vertex 31.551052 71.337852 23.000000
    endloop
  endfacet
  facet normal 0.515590 0.856836 -0.000000
    outer loop
      vertex 31.625275 71.293190 22.000000
      vertex 31.551052 71.337852 23.000000
      vertex 31.625275 71.293190 23.000000
    endloop
  endfacet
  facet normal 0.370158 0.928969 0.000000
    outer loop
      vertex 31.785976 71.229156 22.000000
      vertex 31.625275 71.293190 22.000000
      vertex 31.625275 71.293190 23.000000
    endloop
  endfacet
  facet normal 0.370158 0.928969 -0.000000
    outer loop
      vertex 31.785976 71.229156 22.000000
      vertex 31.625275 71.293190 23.000000
      vertex 31.785976 71.229156 23.000000
    endloop
  endfacet
  facet normal 0.161770 0.986828 0.000000
    outer loop
      vertex 31.956688 71.201172 22.000000
      vertex 31.785976 71.229156 22.000000
      vertex 31.785976 71.229156 23.000000
    endloop
  endfacet
  facet normal 0.161770 0.986828 -0.000000
    outer loop
      vertex 31.956688 71.201172 22.000000
      vertex 31.785976 71.229156 23.000000
      vertex 31.956688 71.201172 23.000000
    endloop
  endfacet
  facet normal -0.054158 0.998532 0.000000
    outer loop
      vertex 32.129425 71.210541 22.000000
      vertex 31.956688 71.201172 22.000000
      vertex 31.956688 71.201172 23.000000
    endloop
  endfacet
  facet normal -0.054158 0.998532 0.000000
    outer loop
      vertex 32.129425 71.210541 22.000000
      vertex 31.956688 71.201172 23.000000
      vertex 32.129425 71.210541 23.000000
    endloop
  endfacet
  facet normal -0.267490 0.963561 0.000000
    outer loop
      vertex 32.296108 71.256813 22.000000
      vertex 32.129425 71.210541 22.000000
      vertex 32.129425 71.210541 23.000000
    endloop
  endfacet
  facet normal -0.267490 0.963561 0.000000
    outer loop
      vertex 32.296108 71.256813 22.000000
      vertex 32.129425 71.210541 23.000000
      vertex 32.296108 71.256813 23.000000
    endloop
  endfacet
  facet normal -0.468440 0.883495 0.000000
    outer loop
      vertex 32.448952 71.337852 22.000000
      vertex 32.296108 71.256813 22.000000
      vertex 32.296108 71.256813 23.000000
    endloop
  endfacet
  facet normal -0.468440 0.883495 0.000000
    outer loop
      vertex 32.448952 71.337852 22.000000
      vertex 32.296108 71.256813 23.000000
      vertex 32.448952 71.337852 23.000000
    endloop
  endfacet
  facet normal -0.647371 0.762175 0.000000
    outer loop
      vertex 32.580795 71.449837 22.000000
      vertex 32.448952 71.337852 22.000000
      vertex 32.448952 71.337852 23.000000
    endloop
  endfacet
  facet normal -0.647371 0.762175 0.000000
    outer loop
      vertex 32.580795 71.449837 22.000000
      vertex 32.448952 71.337852 23.000000
      vertex 32.580795 71.449837 23.000000
    endloop
  endfacet
  facet normal -0.796093 0.605174 0.000000
    outer loop
      vertex 32.685486 71.587555 22.000000
      vertex 32.580795 71.449837 22.000000
      vertex 32.580795 71.449837 23.000000
    endloop
  endfacet
  facet normal -0.796093 0.605174 0.000000
    outer loop
      vertex 32.685486 71.587555 22.000000
      vertex 32.580795 71.449837 23.000000
      vertex 32.685486 71.587555 23.000000
    endloop
  endfacet
  facet normal -0.907573 0.419894 0.000000
    outer loop
      vertex 32.758125 71.744560 22.000000
      vertex 32.685486 71.587555 22.000000
      vertex 32.685486 71.587555 23.000000
    endloop
  endfacet
  facet normal -0.907573 0.419894 0.000000
    outer loop
      vertex 32.758125 71.744560 22.000000
      vertex 32.685486 71.587555 23.000000
      vertex 32.758125 71.744560 23.000000
    endloop
  endfacet
  facet normal -0.976623 0.214959 0.000000
    outer loop
      vertex 32.795311 71.913506 22.000000
      vertex 32.758125 71.744560 22.000000
      vertex 32.758125 71.744560 23.000000
    endloop
  endfacet
  facet normal -0.976623 0.214959 0.000000
    outer loop
      vertex 32.795311 71.913506 22.000000
      vertex 32.758125 71.744560 23.000000
      vertex 32.795311 71.913506 23.000000
    endloop
  endfacet
  facet normal -0.998534 0.054124 0.000000
    outer loop
      vertex 32.799999 72.000000 22.000000
      vertex 32.795311 71.913506 22.000000
      vertex 32.795311 71.913506 23.000000
    endloop
  endfacet
  facet normal -0.998534 0.054124 0.000000
    outer loop
      vertex 32.799999 72.000000 22.000000
      vertex 32.795311 71.913506 23.000000
      vertex 32.799999 72.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 -1.000000 22.000000
      vertex 32.799999 -1.000000 22.000000
      vertex 32.781296 -0.828024 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 -1.000000 22.000000
      vertex 32.685486 -1.412443 22.000000
      vertex 32.758125 -1.255441 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 -1.000000 22.000000
      vertex 32.758125 -1.255441 22.000000
      vertex 32.795311 -1.086495 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.799999 -1.000000 22.000000
      vertex 32.000000 -1.000000 22.000000
      vertex 32.795311 -1.086495 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 -1.000000 22.000000
      vertex 32.296108 -1.743181 22.000000
      vertex 32.448952 -1.662151 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 -1.000000 22.000000
      vertex 32.448952 -1.662151 22.000000
      vertex 32.580795 -1.550160 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.685486 -1.412443 22.000000
      vertex 32.000000 -1.000000 22.000000
      vertex 32.580795 -1.550160 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 -1.000000 22.000000
      vertex 31.785976 -1.770840 22.000000
      vertex 31.956688 -1.798827 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 -1.000000 22.000000
      vertex 31.956688 -1.798827 22.000000
      vertex 32.129425 -1.789461 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.296108 -1.743181 22.000000
      vertex 32.000000 -1.000000 22.000000
      vertex 32.129425 -1.789461 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 -1.000000 22.000000
      vertex 31.482090 -1.609730 22.000000
      vertex 31.551052 -1.662151 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 -1.000000 22.000000
      vertex 31.551052 -1.662151 22.000000
      vertex 31.625275 -1.706810 22.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 31.785976 -1.770840 22.000000
      vertex 32.000000 -1.000000 22.000000
      vertex 31.625275 -1.706810 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 -1.000000 22.000000
      vertex 31.218704 -1.171976 22.000000
      vertex 31.273939 -1.335911 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 -1.000000 22.000000
      vertex 31.273939 -1.335911 22.000000
      vertex 31.363127 -1.484139 22.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 31.482090 -1.609730 22.000000
      vertex 32.000000 -1.000000 22.000000
      vertex 31.363127 -1.484139 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 -1.000000 22.000000
      vertex 31.273939 -0.664089 22.000000
      vertex 31.218704 -0.828024 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 -1.000000 22.000000
      vertex 31.218704 -0.828024 22.000000
      vertex 31.199999 -1.000000 22.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 31.218704 -1.171976 22.000000
      vertex 32.000000 -1.000000 22.000000
      vertex 31.199999 -1.000000 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 -1.000000 22.000000
      vertex 31.551052 -0.337849 22.000000
      vertex 31.482090 -0.390270 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 -1.000000 22.000000
      vertex 31.482090 -0.390270 22.000000
      vertex 31.363127 -0.515861 22.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 31.273939 -0.664089 22.000000
      vertex 32.000000 -1.000000 22.000000
      vertex 31.363127 -0.515861 22.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 32.000000 -1.000000 22.000000
      vertex 32.043312 -0.201173 22.000000
      vertex 31.870573 -0.210539 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 -1.000000 22.000000
      vertex 31.870573 -0.210539 22.000000
      vertex 31.703890 -0.256819 22.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 31.551052 -0.337849 22.000000
      vertex 32.000000 -1.000000 22.000000
      vertex 31.703890 -0.256819 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 -1.000000 22.000000
      vertex 32.517910 -0.390270 22.000000
      vertex 32.374729 -0.293190 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 -1.000000 22.000000
      vertex 32.374729 -0.293190 22.000000
      vertex 32.214024 -0.229160 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.043312 -0.201173 22.000000
      vertex 32.000000 -1.000000 22.000000
      vertex 32.214024 -0.229160 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 -1.000000 22.000000
      vertex 32.781296 -0.828024 22.000000
      vertex 32.726059 -0.664089 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 -1.000000 22.000000
      vertex 32.726059 -0.664089 22.000000
      vertex 32.636875 -0.515861 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.517910 -0.390270 22.000000
      vertex 32.000000 -1.000000 22.000000
      vertex 32.636875 -0.515861 22.000000
    endloop
  endfacet
  facet normal -0.994138 -0.108119 0.000000
    outer loop
      vertex -0.218704 -0.828024 22.000000
      vertex -0.200000 -1.000000 22.000000
      vertex -0.200000 -1.000000 23.000000
    endloop
  endfacet
  facet normal -0.994138 -0.108119 0.000000
    outer loop
      vertex -0.218704 -0.828024 22.000000
      vertex -0.200000 -1.000000 23.000000
      vertex -0.218704 -0.828024 23.000000
    endloop
  endfacet
  facet normal -0.947653 -0.319302 0.000000
    outer loop
      vertex -0.273940 -0.664089 22.000000
      vertex -0.218704 -0.828024 22.000000
      vertex -0.218704 -0.828024 23.000000
    endloop
  endfacet
  facet normal -0.947653 -0.319302 0.000000
    outer loop
      vertex -0.273940 -0.664089 22.000000
      vertex -0.218704 -0.828024 23.000000
      vertex -0.273940 -0.664089 23.000000
    endloop
  endfacet
  facet normal -0.856857 -0.515554 0.000000
    outer loop
      vertex -0.363126 -0.515861 22.000000
      vertex -0.273940 -0.664089 22.000000
      vertex -0.273940 -0.664089 23.000000
    endloop
  endfacet
  facet normal -0.856857 -0.515554 0.000000
    outer loop
      vertex -0.363126 -0.515861 22.000000
      vertex -0.273940 -0.664089 23.000000
      vertex -0.363126 -0.515861 23.000000
    endloop
  endfacet
  facet normal -0.725995 -0.687699 0.000000
    outer loop
      vertex -0.482091 -0.390270 22.000000
      vertex -0.363126 -0.515861 22.000000
      vertex -0.363126 -0.515861 23.000000
    endloop
  endfacet
  facet normal -0.725995 -0.687699 0.000000
    outer loop
      vertex -0.482091 -0.390270 22.000000
      vertex -0.363126 -0.515861 23.000000
      vertex -0.482091 -0.390270 23.000000
    endloop
  endfacet
  facet normal -0.561187 -0.827689 0.000000
    outer loop
      vertex -0.625273 -0.293190 22.000000
      vertex -0.482091 -0.390270 22.000000
      vertex -0.482091 -0.390270 23.000000
    endloop
  endfacet
  facet normal -0.561187 -0.827689 0.000000
    outer loop
      vertex -0.625273 -0.293190 22.000000
      vertex -0.482091 -0.390270 23.000000
      vertex -0.625273 -0.293190 23.000000
    endloop
  endfacet
  facet normal -0.370138 -0.928977 0.000000
    outer loop
      vertex -0.785977 -0.229160 22.000000
      vertex -0.625273 -0.293190 22.000000
      vertex -0.625273 -0.293190 23.000000
    endloop
  endfacet
  facet normal -0.370138 -0.928977 0.000000
    outer loop
      vertex -0.785977 -0.229160 22.000000
      vertex -0.625273 -0.293190 23.000000
      vertex -0.785977 -0.229160 23.000000
    endloop
  endfacet
  facet normal -0.161782 -0.986827 0.000000
    outer loop
      vertex -0.956689 -0.201173 22.000000
      vertex -0.785977 -0.229160 22.000000
      vertex -0.785977 -0.229160 23.000000
    endloop
  endfacet
  facet normal -0.161782 -0.986827 0.000000
    outer loop
      vertex -0.956689 -0.201173 22.000000
      vertex -0.785977 -0.229160 23.000000
      vertex -0.956689 -0.201173 23.000000
    endloop
  endfacet
  facet normal 0.054139 -0.998533 0.000000
    outer loop
      vertex -1.129426 -0.210539 22.000000
      vertex -0.956689 -0.201173 22.000000
      vertex -0.956689 -0.201173 23.000000
    endloop
  endfacet
  facet normal 0.054139 -0.998533 0.000000
    outer loop
      vertex -1.129426 -0.210539 22.000000
      vertex -0.956689 -0.201173 23.000000
      vertex -1.129426 -0.210539 23.000000
    endloop
  endfacet
  facet normal 0.267528 -0.963550 0.000000
    outer loop
      vertex -1.296111 -0.256819 22.000000
      vertex -1.129426 -0.210539 22.000000
      vertex -1.129426 -0.210539 23.000000
    endloop
  endfacet
  facet normal 0.267528 -0.963550 0.000000
    outer loop
      vertex -1.296111 -0.256819 22.000000
      vertex -1.129426 -0.210539 23.000000
      vertex -1.296111 -0.256819 23.000000
    endloop
  endfacet
  facet normal 0.468408 -0.883512 0.000000
    outer loop
      vertex -1.448950 -0.337849 22.000000
      vertex -1.296111 -0.256819 22.000000
      vertex -1.296111 -0.256819 23.000000
    endloop
  endfacet
  facet normal 0.468408 -0.883512 0.000000
    outer loop
      vertex -1.448950 -0.337849 22.000000
      vertex -1.296111 -0.256819 23.000000
      vertex -1.448950 -0.337849 23.000000
    endloop
  endfacet
  facet normal 0.605174 -0.796093 0.000000
    outer loop
      vertex -1.517909 -0.390270 22.000000
      vertex -1.448950 -0.337849 22.000000
      vertex -1.448950 -0.337849 23.000000
    endloop
  endfacet
  facet normal 0.605174 -0.796093 0.000000
    outer loop
      vertex -1.517909 -0.390270 22.000000
      vertex -1.448950 -0.337849 23.000000
      vertex -1.517909 -0.390270 23.000000
    endloop
  endfacet
  facet normal 0.725996 -0.687699 0.000000
    outer loop
      vertex -1.636874 -0.515861 22.000000
      vertex -1.517909 -0.390270 22.000000
      vertex -1.517909 -0.390270 23.000000
    endloop
  endfacet
  facet normal 0.725996 -0.687699 0.000000
    outer loop
      vertex -1.636874 -0.515861 22.000000
      vertex -1.517909 -0.390270 23.000000
      vertex -1.636874 -0.515861 23.000000
    endloop
  endfacet
  facet normal 0.856857 -0.515554 0.000000
    outer loop
      vertex -1.726060 -0.664089 22.000000
      vertex -1.636874 -0.515861 22.000000
      vertex -1.636874 -0.515861 23.000000
    endloop
  endfacet
  facet normal 0.856857 -0.515554 0.000000
    outer loop
      vertex -1.726060 -0.664089 22.000000
      vertex -1.636874 -0.515861 23.000000
      vertex -1.726060 -0.664089 23.000000
    endloop
  endfacet
  facet normal 0.947653 -0.319302 0.000000
    outer loop
      vertex -1.781296 -0.828024 22.000000
      vertex -1.726060 -0.664089 22.000000
      vertex -1.726060 -0.664089 23.000000
    endloop
  endfacet
  facet normal 0.947653 -0.319302 0.000000
    outer loop
      vertex -1.781296 -0.828024 22.000000
      vertex -1.726060 -0.664089 23.000000
      vertex -1.781296 -0.828024 23.000000
    endloop
  endfacet
  facet normal 0.994138 -0.108118 0.000000
    outer loop
      vertex -1.800000 -1.000000 22.000000
      vertex -1.781296 -0.828024 22.000000
      vertex -1.781296 -0.828024 23.000000
    endloop
  endfacet
  facet normal 0.994138 -0.108118 0.000000
    outer loop
      vertex -1.800000 -1.000000 22.000000
      vertex -1.781296 -0.828024 23.000000
      vertex -1.800000 -1.000000 23.000000
    endloop
  endfacet
  facet normal 0.994138 0.108118 0.000000
    outer loop
      vertex -1.781296 -1.171976 22.000000
      vertex -1.800000 -1.000000 22.000000
      vertex -1.800000 -1.000000 23.000000
    endloop
  endfacet
  facet normal 0.994138 0.108118 -0.000000
    outer loop
      vertex -1.781296 -1.171976 22.000000
      vertex -1.800000 -1.000000 23.000000
      vertex -1.781296 -1.171976 23.000000
    endloop
  endfacet
  facet normal 0.947653 0.319302 0.000000
    outer loop
      vertex -1.726060 -1.335911 22.000000
      vertex -1.781296 -1.171976 22.000000
      vertex -1.781296 -1.171976 23.000000
    endloop
  endfacet
  facet normal 0.947653 0.319302 -0.000000
    outer loop
      vertex -1.726060 -1.335911 22.000000
      vertex -1.781296 -1.171976 23.000000
      vertex -1.726060 -1.335911 23.000000
    endloop
  endfacet
  facet normal 0.856857 0.515554 0.000000
    outer loop
      vertex -1.636874 -1.484139 22.000000
      vertex -1.726060 -1.335911 22.000000
      vertex -1.726060 -1.335911 23.000000
    endloop
  endfacet
  facet normal 0.856857 0.515554 -0.000000
    outer loop
      vertex -1.636874 -1.484139 22.000000
      vertex -1.726060 -1.335911 23.000000
      vertex -1.636874 -1.484139 23.000000
    endloop
  endfacet
  facet normal 0.725996 0.687699 0.000000
    outer loop
      vertex -1.517909 -1.609730 22.000000
      vertex -1.636874 -1.484139 22.000000
      vertex -1.636874 -1.484139 23.000000
    endloop
  endfacet
  facet normal 0.725996 0.687699 -0.000000
    outer loop
      vertex -1.517909 -1.609730 22.000000
      vertex -1.636874 -1.484139 23.000000
      vertex -1.517909 -1.609730 23.000000
    endloop
  endfacet
  facet normal 0.605174 0.796093 0.000000
    outer loop
      vertex -1.448950 -1.662151 22.000000
      vertex -1.517909 -1.609730 22.000000
      vertex -1.517909 -1.609730 23.000000
    endloop
  endfacet
  facet normal 0.605174 0.796093 -0.000000
    outer loop
      vertex -1.448950 -1.662151 22.000000
      vertex -1.517909 -1.609730 23.000000
      vertex -1.448950 -1.662151 23.000000
    endloop
  endfacet
  facet normal 0.515554 0.856857 0.000000
    outer loop
      vertex -1.374727 -1.706810 22.000000
      vertex -1.448950 -1.662151 22.000000
      vertex -1.448950 -1.662151 23.000000
    endloop
  endfacet
  facet normal 0.515554 0.856857 -0.000000
    outer loop
      vertex -1.374727 -1.706810 22.000000
      vertex -1.448950 -1.662151 23.000000
      vertex -1.374727 -1.706810 23.000000
    endloop
  endfacet
  facet normal 0.370138 0.928977 0.000000
    outer loop
      vertex -1.214023 -1.770840 22.000000
      vertex -1.374727 -1.706810 22.000000
      vertex -1.374727 -1.706810 23.000000
    endloop
  endfacet
  facet normal 0.370138 0.928977 -0.000000
    outer loop
      vertex -1.214023 -1.770840 22.000000
      vertex -1.374727 -1.706810 23.000000
      vertex -1.214023 -1.770840 23.000000
    endloop
  endfacet
  facet normal 0.161782 0.986827 0.000000
    outer loop
      vertex -1.043311 -1.798827 22.000000
      vertex -1.214023 -1.770840 22.000000
      vertex -1.214023 -1.770840 23.000000
    endloop
  endfacet
  facet normal 0.161782 0.986827 -0.000000
    outer loop
      vertex -1.043311 -1.798827 22.000000
      vertex -1.214023 -1.770840 23.000000
      vertex -1.043311 -1.798827 23.000000
    endloop
  endfacet
  facet normal -0.054138 0.998533 0.000000
    outer loop
      vertex -0.870574 -1.789461 22.000000
      vertex -1.043311 -1.798827 22.000000
      vertex -1.043311 -1.798827 23.000000
    endloop
  endfacet
  facet normal -0.054138 0.998533 0.000000
    outer loop
      vertex -0.870574 -1.789461 22.000000
      vertex -1.043311 -1.798827 23.000000
      vertex -0.870574 -1.789461 23.000000
    endloop
  endfacet
  facet normal -0.267529 0.963550 0.000000
    outer loop
      vertex -0.703889 -1.743181 22.000000
      vertex -0.870574 -1.789461 22.000000
      vertex -0.870574 -1.789461 23.000000
    endloop
  endfacet
  facet normal -0.267529 0.963550 0.000000
    outer loop
      vertex -0.703889 -1.743181 22.000000
      vertex -0.870574 -1.789461 23.000000
      vertex -0.703889 -1.743181 23.000000
    endloop
  endfacet
  facet normal -0.468408 0.883512 0.000000
    outer loop
      vertex -0.551050 -1.662151 22.000000
      vertex -0.703889 -1.743181 22.000000
      vertex -0.703889 -1.743181 23.000000
    endloop
  endfacet
  facet normal -0.468408 0.883512 0.000000
    outer loop
      vertex -0.551050 -1.662151 22.000000
      vertex -0.703889 -1.743181 23.000000
      vertex -0.551050 -1.662151 23.000000
    endloop
  endfacet
  facet normal -0.647386 0.762162 0.000000
    outer loop
      vertex -0.419204 -1.550160 22.000000
      vertex -0.551050 -1.662151 22.000000
      vertex -0.551050 -1.662151 23.000000
    endloop
  endfacet
  facet normal -0.647386 0.762162 0.000000
    outer loop
      vertex -0.419204 -1.550160 22.000000
      vertex -0.551050 -1.662151 23.000000
      vertex -0.419204 -1.550160 23.000000
    endloop
  endfacet
  facet normal -0.796093 0.605174 0.000000
    outer loop
      vertex -0.314514 -1.412443 22.000000
      vertex -0.419204 -1.550160 22.000000
      vertex -0.419204 -1.550160 23.000000
    endloop
  endfacet
  facet normal -0.796093 0.605174 0.000000
    outer loop
      vertex -0.314514 -1.412443 22.000000
      vertex -0.419204 -1.550160 23.000000
      vertex -0.314514 -1.412443 23.000000
    endloop
  endfacet
  facet normal -0.907575 0.419889 0.000000
    outer loop
      vertex -0.241877 -1.255441 22.000000
      vertex -0.314514 -1.412443 22.000000
      vertex -0.314514 -1.412443 23.000000
    endloop
  endfacet
  facet normal -0.907575 0.419889 0.000000
    outer loop
      vertex -0.241877 -1.255441 22.000000
      vertex -0.314514 -1.412443 23.000000
      vertex -0.241877 -1.255441 23.000000
    endloop
  endfacet
  facet normal -0.976621 0.214971 0.000000
    outer loop
      vertex -0.204690 -1.086495 22.000000
      vertex -0.241877 -1.255441 22.000000
      vertex -0.241877 -1.255441 23.000000
    endloop
  endfacet
  facet normal -0.976621 0.214971 0.000000
    outer loop
      vertex -0.204690 -1.086495 22.000000
      vertex -0.241877 -1.255441 23.000000
      vertex -0.204690 -1.086495 23.000000
    endloop
  endfacet
  facet normal -0.998533 0.054139 0.000000
    outer loop
      vertex -0.200000 -1.000000 22.000000
      vertex -0.204690 -1.086495 22.000000
      vertex -0.204690 -1.086495 23.000000
    endloop
  endfacet
  facet normal -0.998533 0.054139 0.000000
    outer loop
      vertex -0.200000 -1.000000 22.000000
      vertex -0.204690 -1.086495 23.000000
      vertex -0.200000 -1.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 22.250000 -2.000000 -4.500000
      vertex 9.250000 -2.000000 -4.500000
      vertex 9.250000 -1.000000 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 22.250000 -2.000000 -4.500000
      vertex 9.250000 -1.000000 -4.500000
      vertex 22.250000 -1.000000 -4.500000
    endloop
  endfacet
  facet normal -0.284005 0.958823 0.000000
    outer loop
      vertex -1.888229 7.948888 20.551111
      vertex -1.888229 7.948888 15.948888
      vertex -1.963526 7.926585 15.926584
    endloop
  endfacet
  facet normal -0.382675 0.923883 0.000000
    outer loop
      vertex -2.037552 7.900370 20.599630
      vertex -2.037552 7.900370 15.900370
      vertex -2.110105 7.870318 15.870317
    endloop
  endfacet
  facet normal -0.477155 0.878819 0.000000
    outer loop
      vertex -2.180986 7.836510 20.663490
      vertex -2.180986 7.836510 15.836509
      vertex -2.250000 7.799038 15.799038
    endloop
  endfacet
  facet normal -0.998630 0.052337 0.000000
    outer loop
      vertex -2.991783 6.656793 21.843208
      vertex -3.000000 6.500000 14.500000
      vertex -3.000000 6.500000 22.000000
    endloop
  endfacet
  facet normal -0.998630 0.052337 0.000000
    outer loop
      vertex -2.991783 6.656793 14.656793
      vertex -3.000000 6.500000 14.500000
      vertex -2.991783 6.656793 21.843208
    endloop
  endfacet
  facet normal -0.987689 0.156433 0.000000
    outer loop
      vertex -2.991783 6.656793 14.656793
      vertex -2.991783 6.656793 21.843208
      vertex -2.967221 6.811867 21.688131
    endloop
  endfacet
  facet normal -0.987689 0.156433 0.000000
    outer loop
      vertex -2.967221 6.811867 14.811868
      vertex -2.991783 6.656793 14.656793
      vertex -2.967221 6.811867 21.688131
    endloop
  endfacet
  facet normal -0.965926 0.258820 0.000000
    outer loop
      vertex -2.967221 6.811867 14.811868
      vertex -2.967221 6.811867 21.688131
      vertex -2.926585 6.963525 21.536474
    endloop
  endfacet
  facet normal -0.965926 0.258820 0.000000
    outer loop
      vertex -2.926585 6.963525 14.963526
      vertex -2.967221 6.811867 14.811868
      vertex -2.926585 6.963525 21.536474
    endloop
  endfacet
  facet normal -0.933581 0.358367 0.000000
    outer loop
      vertex -2.926585 6.963525 14.963526
      vertex -2.926585 6.963525 21.536474
      vertex -2.870318 7.110105 21.389894
    endloop
  endfacet
  facet normal -0.933581 0.358367 0.000000
    outer loop
      vertex -2.870318 7.110105 15.110106
      vertex -2.926585 6.963525 14.963526
      vertex -2.870318 7.110105 21.389894
    endloop
  endfacet
  facet normal -0.891007 0.453990 0.000000
    outer loop
      vertex -2.870318 7.110105 15.110106
      vertex -2.870318 7.110105 21.389894
      vertex -2.799038 7.250000 21.250000
    endloop
  endfacet
  facet normal -0.891007 0.453990 0.000000
    outer loop
      vertex -2.799038 7.250000 15.250000
      vertex -2.870318 7.110105 15.110106
      vertex -2.799038 7.250000 21.250000
    endloop
  endfacet
  facet normal -0.838671 0.544638 0.000000
    outer loop
      vertex -2.799038 7.250000 15.250000
      vertex -2.799038 7.250000 21.250000
      vertex -2.713526 7.381678 21.118322
    endloop
  endfacet
  facet normal -0.838671 0.544638 0.000000
    outer loop
      vertex -2.713526 7.381678 15.381678
      vertex -2.799038 7.250000 15.250000
      vertex -2.713526 7.381678 21.118322
    endloop
  endfacet
  facet normal -0.777145 0.629321 0.000000
    outer loop
      vertex -2.713526 7.381678 15.381678
      vertex -2.713526 7.381678 21.118322
      vertex -2.614717 7.503696 20.996304
    endloop
  endfacet
  facet normal -0.777145 0.629321 0.000000
    outer loop
      vertex -2.614717 7.503696 15.503696
      vertex -2.713526 7.381678 15.381678
      vertex -2.614717 7.503696 20.996304
    endloop
  endfacet
  facet normal -0.707108 0.707106 0.000000
    outer loop
      vertex -2.614717 7.503696 15.503696
      vertex -2.614717 7.503696 20.996304
      vertex -2.503696 7.614717 20.885283
    endloop
  endfacet
  facet normal -0.707108 0.707106 0.000000
    outer loop
      vertex -2.503696 7.614717 15.614717
      vertex -2.614717 7.503696 15.503696
      vertex -2.503696 7.614717 20.885283
    endloop
  endfacet
  facet normal -0.629320 0.777146 0.000000
    outer loop
      vertex -2.503696 7.614717 15.614717
      vertex -2.503696 7.614717 20.885283
      vertex -2.381678 7.713526 20.786476
    endloop
  endfacet
  facet normal -0.629320 0.777146 0.000000
    outer loop
      vertex -2.381678 7.713526 15.713526
      vertex -2.503696 7.614717 15.614717
      vertex -2.381678 7.713526 20.786476
    endloop
  endfacet
  facet normal -0.566405 0.824127 0.000000
    outer loop
      vertex -2.381678 7.713526 15.713526
      vertex -2.381678 7.713526 20.786476
      vertex -2.316958 7.758006 20.741993
    endloop
  endfacet
  facet normal -0.566405 0.824127 0.000000
    outer loop
      vertex -2.316958 7.758006 15.758006
      vertex -2.381678 7.713526 15.713526
      vertex -2.316958 7.758006 20.741993
    endloop
  endfacet
  facet normal -0.522500 0.852639 0.000000
    outer loop
      vertex -2.250000 7.799038 15.799038
      vertex -2.316958 7.758006 15.758006
      vertex -2.316958 7.758006 20.741993
    endloop
  endfacet
  facet normal -0.522500 0.852639 0.000000
    outer loop
      vertex -2.250000 7.799038 15.799038
      vertex -2.316958 7.758006 20.741993
      vertex -2.250000 7.799038 20.700962
    endloop
  endfacet
  facet normal -0.477155 0.878819 0.000000
    outer loop
      vertex -2.180986 7.836510 20.663490
      vertex -2.250000 7.799038 15.799038
      vertex -2.250000 7.799038 20.700962
    endloop
  endfacet
  facet normal -0.430515 0.902583 0.000000
    outer loop
      vertex -2.110105 7.870318 15.870317
      vertex -2.180986 7.836510 15.836509
      vertex -2.180986 7.836510 20.663490
    endloop
  endfacet
  facet normal -0.430515 0.902583 0.000000
    outer loop
      vertex -2.110105 7.870318 15.870317
      vertex -2.180986 7.836510 20.663490
      vertex -2.110105 7.870318 20.629683
    endloop
  endfacet
  facet normal -0.382675 0.923883 0.000000
    outer loop
      vertex -2.037552 7.900370 20.599630
      vertex -2.110105 7.870318 15.870317
      vertex -2.110105 7.870318 20.629683
    endloop
  endfacet
  facet normal -0.333818 0.942638 0.000000
    outer loop
      vertex -1.963526 7.926585 15.926584
      vertex -2.037552 7.900370 15.900370
      vertex -2.037552 7.900370 20.599630
    endloop
  endfacet
  facet normal -0.333818 0.942638 0.000000
    outer loop
      vertex -1.963526 7.926585 15.926584
      vertex -2.037552 7.900370 20.599630
      vertex -1.963526 7.926585 20.573416
    endloop
  endfacet
  facet normal -0.284005 0.958823 0.000000
    outer loop
      vertex -1.888229 7.948888 20.551111
      vertex -1.963526 7.926585 15.926584
      vertex -1.963526 7.926585 20.573416
    endloop
  endfacet
  facet normal -0.233455 0.972368 0.000000
    outer loop
      vertex -1.811868 7.967222 15.967222
      vertex -1.888229 7.948888 15.948888
      vertex -1.888229 7.948888 20.551111
    endloop
  endfacet
  facet normal -0.233455 0.972368 0.000000
    outer loop
      vertex -1.811868 7.967222 15.967222
      vertex -1.888229 7.948888 20.551111
      vertex -1.811868 7.967222 20.532780
    endloop
  endfacet
  facet normal -0.182226 0.983257 0.000000
    outer loop
      vertex -1.734652 7.981532 20.518467
      vertex -1.811868 7.967222 15.967222
      vertex -1.811868 7.967222 20.532780
    endloop
  endfacet
  facet normal -0.026182 0.999657 0.000000
    outer loop
      vertex -1.578504 7.997944 20.502054
      vertex -1.500000 8.000000 20.500000
      vertex -1.500000 8.000000 16.000000
    endloop
  endfacet
  facet normal -0.026182 0.999657 0.000000
    outer loop
      vertex -1.578504 7.997944 20.502054
      vertex -1.500000 8.000000 16.000000
      vertex -1.578504 7.997944 15.997945
    endloop
  endfacet
  facet normal -0.078462 0.996917 0.000000
    outer loop
      vertex -1.656793 7.991782 20.508217
      vertex -1.578504 7.997944 20.502054
      vertex -1.578504 7.997944 15.997945
    endloop
  endfacet
  facet normal -0.078462 0.996917 0.000000
    outer loop
      vertex -1.656793 7.991782 20.508217
      vertex -1.578504 7.997944 15.997945
      vertex -1.656793 7.991782 15.991783
    endloop
  endfacet
  facet normal -0.130523 0.991445 0.000000
    outer loop
      vertex -1.734652 7.981532 20.518467
      vertex -1.656793 7.991782 20.508217
      vertex -1.656793 7.991782 15.991783
    endloop
  endfacet
  facet normal -0.130523 0.991445 0.000000
    outer loop
      vertex -1.734652 7.981532 20.518467
      vertex -1.656793 7.991782 15.991783
      vertex -1.734652 7.981532 15.981533
    endloop
  endfacet
  facet normal -0.182226 0.983257 0.000000
    outer loop
      vertex -1.811868 7.967222 15.967222
      vertex -1.734652 7.981532 20.518467
      vertex -1.734652 7.981532 15.981533
    endloop
  endfacet
  facet normal -1.000000 0.000000 0.000000
    outer loop
      vertex 3.000000 0.000000 -4.500000
      vertex 3.000000 3.000000 -4.500000
      vertex 3.000000 3.000000 -6.500000
    endloop
  endfacet
  facet normal -1.000000 0.000000 0.000000
    outer loop
      vertex 3.000000 0.000000 -4.500000
      vertex 3.000000 3.000000 -6.500000
      vertex 3.000000 0.000000 -6.500000
    endloop
  endfacet
  facet normal 0.891008 -0.453988 0.000000
    outer loop
      vertex 9.163546 -2.406737 -6.086455
      vertex 9.163546 -2.406737 -4.413546
      vertex 9.116026 -2.500000 -4.366025
    endloop
  endfacet
  facet normal 0.777151 -0.629314 0.000000
    outer loop
      vertex 9.059016 -2.587785 -6.190983
      vertex 9.059016 -2.587785 -4.309017
      vertex 8.993145 -2.669131 -4.243145
    endloop
  endfacet
  facet normal 0.629320 -0.777147 0.000000
    outer loop
      vertex 8.919131 -2.743145 -6.330870
      vertex 8.919131 -2.743145 -4.169131
      vertex 8.837786 -2.809017 -4.087785
    endloop
  endfacet
  facet normal 0.052334 -0.998630 0.000000
    outer loop
      vertex 8.354528 -2.994522 -6.895472
      vertex 8.354528 -2.994522 -3.604528
      vertex 8.250000 -3.000000 -3.500000
    endloop
  endfacet
  facet normal 0.052334 -0.998630 0.000000
    outer loop
      vertex 8.354528 -2.994522 -6.895472
      vertex 8.250000 -3.000000 -3.500000
      vertex 8.250000 -3.000000 -7.000000
    endloop
  endfacet
  facet normal 0.156434 -0.987688 0.000000
    outer loop
      vertex 8.457912 -2.978148 -3.707911
      vertex 8.354528 -2.994522 -3.604528
      vertex 8.354528 -2.994522 -6.895472
    endloop
  endfacet
  facet normal 0.156434 -0.987688 0.000000
    outer loop
      vertex 8.457912 -2.978148 -3.707911
      vertex 8.354528 -2.994522 -6.895472
      vertex 8.457912 -2.978148 -6.792089
    endloop
  endfacet
  facet normal 0.258822 -0.965925 0.000000
    outer loop
      vertex 8.559017 -2.951056 -3.809017
      vertex 8.457912 -2.978148 -3.707911
      vertex 8.457912 -2.978148 -6.792089
    endloop
  endfacet
  facet normal 0.258822 -0.965925 0.000000
    outer loop
      vertex 8.559017 -2.951056 -3.809017
      vertex 8.457912 -2.978148 -6.792089
      vertex 8.559017 -2.951056 -6.690983
    endloop
  endfacet
  facet normal 0.358370 -0.933580 0.000000
    outer loop
      vertex 8.656736 -2.913545 -3.906737
      vertex 8.559017 -2.951056 -3.809017
      vertex 8.559017 -2.951056 -6.690983
    endloop
  endfacet
  facet normal 0.358370 -0.933580 0.000000
    outer loop
      vertex 8.656736 -2.913545 -3.906737
      vertex 8.559017 -2.951056 -6.690983
      vertex 8.656736 -2.913545 -6.593263
    endloop
  endfacet
  facet normal 0.453990 -0.891007 0.000000
    outer loop
      vertex 8.750000 -2.866025 -4.000000
      vertex 8.656736 -2.913545 -3.906737
      vertex 8.656736 -2.913545 -6.593263
    endloop
  endfacet
  facet normal 0.453990 -0.891007 0.000000
    outer loop
      vertex 8.750000 -2.866025 -4.000000
      vertex 8.656736 -2.913545 -6.593263
      vertex 8.750000 -2.866025 -6.500000
    endloop
  endfacet
  facet normal 0.544636 -0.838673 0.000000
    outer loop
      vertex 8.837786 -2.809017 -4.087785
      vertex 8.750000 -2.866025 -4.000000
      vertex 8.750000 -2.866025 -6.500000
    endloop
  endfacet
  facet normal 0.544636 -0.838673 0.000000
    outer loop
      vertex 8.837786 -2.809017 -4.087785
      vertex 8.750000 -2.866025 -6.500000
      vertex 8.837786 -2.809017 -6.412215
    endloop
  endfacet
  facet normal 0.629320 -0.777147 0.000000
    outer loop
      vertex 8.919131 -2.743145 -6.330870
      vertex 8.837786 -2.809017 -4.087785
      vertex 8.837786 -2.809017 -6.412215
    endloop
  endfacet
  facet normal 0.707108 -0.707106 0.000000
    outer loop
      vertex 8.993145 -2.669131 -4.243145
      vertex 8.919131 -2.743145 -4.169131
      vertex 8.919131 -2.743145 -6.330870
    endloop
  endfacet
  facet normal 0.707108 -0.707106 0.000000
    outer loop
      vertex 8.993145 -2.669131 -4.243145
      vertex 8.919131 -2.743145 -6.330870
      vertex 8.993145 -2.669131 -6.256855
    endloop
  endfacet
  facet normal 0.777151 -0.629314 0.000000
    outer loop
      vertex 9.059016 -2.587785 -6.190983
      vertex 8.993145 -2.669131 -4.243145
      vertex 8.993145 -2.669131 -6.256855
    endloop
  endfacet
  facet normal 0.838665 -0.544648 0.000000
    outer loop
      vertex 9.116026 -2.500000 -4.366025
      vertex 9.059016 -2.587785 -4.309017
      vertex 9.059016 -2.587785 -6.190983
    endloop
  endfacet
  facet normal 0.838665 -0.544648 0.000000
    outer loop
      vertex 9.116026 -2.500000 -4.366025
      vertex 9.059016 -2.587785 -6.190983
      vertex 9.116026 -2.500000 -6.133975
    endloop
  endfacet
  facet normal 0.891008 -0.453988 0.000000
    outer loop
      vertex 9.163546 -2.406737 -6.086455
      vertex 9.116026 -2.500000 -4.366025
      vertex 9.116026 -2.500000 -6.133975
    endloop
  endfacet
  facet normal 0.933581 -0.358366 0.000000
    outer loop
      vertex 9.201056 -2.309017 -4.451056
      vertex 9.163546 -2.406737 -4.413546
      vertex 9.163546 -2.406737 -6.086455
    endloop
  endfacet
  facet normal 0.933581 -0.358366 0.000000
    outer loop
      vertex 9.201056 -2.309017 -4.451056
      vertex 9.163546 -2.406737 -6.086455
      vertex 9.201056 -2.309017 -6.048944
    endloop
  endfacet
  facet normal 0.965926 -0.258819 0.000000
    outer loop
      vertex 9.228148 -2.207912 -4.478148
      vertex 9.201056 -2.309017 -4.451056
      vertex 9.201056 -2.309017 -6.048944
    endloop
  endfacet
  facet normal 0.965926 -0.258819 0.000000
    outer loop
      vertex 9.228148 -2.207912 -4.478148
      vertex 9.201056 -2.309017 -6.048944
      vertex 9.228148 -2.207912 -6.021852
    endloop
  endfacet
  facet normal 0.987688 -0.156437 0.000000
    outer loop
      vertex 9.244522 -2.104528 -4.494522
      vertex 9.228148 -2.207912 -4.478148
      vertex 9.228148 -2.207912 -6.021852
    endloop
  endfacet
  facet normal 0.987688 -0.156437 0.000000
    outer loop
      vertex 9.244522 -2.104528 -4.494522
      vertex 9.228148 -2.207912 -6.021852
      vertex 9.244522 -2.104528 -6.005478
    endloop
  endfacet
  facet normal 0.998630 -0.052334 0.000000
    outer loop
      vertex 9.244522 -2.104528 -4.494522
      vertex 9.244522 -2.104528 -6.005478
      vertex 9.250000 -2.000000 -6.000000
    endloop
  endfacet
  facet normal 0.998630 -0.052334 0.000000
    outer loop
      vertex 9.250000 -2.000000 -4.500000
      vertex 9.244522 -2.104528 -4.494522
      vertex 9.250000 -2.000000 -6.000000
    endloop
  endfacet
  facet normal -0.026158 0.000000 -0.999658
    outer loop
      vertex -1.578504 14.002056 20.502054
      vertex -1.500000 14.000000 20.500000
      vertex -1.500000 8.000000 20.500000
    endloop
  endfacet
  facet normal -0.026158 -0.000000 -0.999658
    outer loop
      vertex -1.578504 14.002056 20.502054
      vertex -1.500000 8.000000 20.500000
      vertex -1.578504 7.997944 20.502054
    endloop
  endfacet
  facet normal -0.078474 0.000000 -0.996916
    outer loop
      vertex -1.656793 14.008218 20.508217
      vertex -1.578504 14.002056 20.502054
      vertex -1.578504 7.997944 20.502054
    endloop
  endfacet
  facet normal -0.078474 -0.000000 -0.996916
    outer loop
      vertex -1.656793 14.008218 20.508217
      vertex -1.578504 7.997944 20.502054
      vertex -1.656793 7.991782 20.508217
    endloop
  endfacet
  facet normal -0.130523 0.000000 -0.991445
    outer loop
      vertex -1.734652 14.018468 20.518467
      vertex -1.656793 14.008218 20.508217
      vertex -1.656793 7.991782 20.508217
    endloop
  endfacet
  facet normal -0.130523 -0.000000 -0.991445
    outer loop
      vertex -1.734652 14.018468 20.518467
      vertex -1.656793 7.991782 20.508217
      vertex -1.734652 7.981532 20.518467
    endloop
  endfacet
  facet normal -0.182255 0.000000 -0.983251
    outer loop
      vertex -1.811868 14.032779 20.532780
      vertex -1.734652 14.018468 20.518467
      vertex -1.734652 7.981532 20.518467
    endloop
  endfacet
  facet normal -0.182255 -0.000000 -0.983251
    outer loop
      vertex -1.811868 14.032779 20.532780
      vertex -1.734652 7.981532 20.518467
      vertex -1.811868 7.967222 20.532780
    endloop
  endfacet
  facet normal -0.233432 0.000000 -0.972373
    outer loop
      vertex -1.888229 14.051111 20.551111
      vertex -1.811868 14.032779 20.532780
      vertex -1.811868 7.967222 20.532780
    endloop
  endfacet
  facet normal -0.233432 -0.000000 -0.972373
    outer loop
      vertex -1.888229 14.051111 20.551111
      vertex -1.811868 7.967222 20.532780
      vertex -1.888229 7.948888 20.551111
    endloop
  endfacet
  facet normal -0.284022 0.000000 -0.958818
    outer loop
      vertex -1.963526 14.073416 20.573416
      vertex -1.888229 14.051111 20.551111
      vertex -1.888229 7.948888 20.551111
    endloop
  endfacet
  facet normal -0.284022 -0.000000 -0.958818
    outer loop
      vertex -1.963526 14.073416 20.573416
      vertex -1.888229 7.948888 20.551111
      vertex -1.963526 7.926585 20.573416
    endloop
  endfacet
  facet normal -0.333812 0.000000 -0.942640
    outer loop
      vertex -2.037552 14.099629 20.599630
      vertex -1.963526 14.073416 20.573416
      vertex -1.963526 7.926585 20.573416
    endloop
  endfacet
  facet normal -0.333812 -0.000000 -0.942640
    outer loop
      vertex -2.037552 14.099629 20.599630
      vertex -1.963526 7.926585 20.573416
      vertex -2.037552 7.900370 20.599630
    endloop
  endfacet
  facet normal -0.382680 0.000000 -0.923881
    outer loop
      vertex -2.110105 14.129682 20.629683
      vertex -2.037552 14.099629 20.599630
      vertex -2.037552 7.900370 20.599630
    endloop
  endfacet
  facet normal -0.382680 -0.000000 -0.923881
    outer loop
      vertex -2.110105 14.129682 20.629683
      vertex -2.037552 7.900370 20.599630
      vertex -2.110105 7.870318 20.629683
    endloop
  endfacet
  facet normal -0.430505 0.000000 -0.902588
    outer loop
      vertex -2.180986 14.163490 20.663490
      vertex -2.110105 14.129682 20.629683
      vertex -2.110105 7.870318 20.629683
    endloop
  endfacet
  facet normal -0.430505 -0.000000 -0.902588
    outer loop
      vertex -2.180986 14.163490 20.663490
      vertex -2.110105 7.870318 20.629683
      vertex -2.180986 7.836510 20.663490
    endloop
  endfacet
  facet normal -0.477159 0.000000 -0.878817
    outer loop
      vertex -2.250000 14.200962 20.700962
      vertex -2.180986 14.163490 20.663490
      vertex -2.180986 7.836510 20.663490
    endloop
  endfacet
  facet normal -0.477159 -0.000000 -0.878817
    outer loop
      vertex -2.250000 14.200962 20.700962
      vertex -2.180986 7.836510 20.663490
      vertex -2.250000 7.799038 20.700962
    endloop
  endfacet
  facet normal -0.522487 0.000000 -0.852647
    outer loop
      vertex -2.316958 14.241994 20.741993
      vertex -2.250000 14.200962 20.700962
      vertex -2.250000 7.799038 20.700962
    endloop
  endfacet
  facet normal -0.522487 -0.000000 -0.852648
    outer loop
      vertex -2.316958 14.241994 20.741993
      vertex -2.250000 7.799038 20.700962
      vertex -2.316958 7.758006 20.741993
    endloop
  endfacet
  facet normal -0.566430 0.000000 -0.824110
    outer loop
      vertex -2.381678 14.286474 20.786476
      vertex -2.316958 14.241994 20.741993
      vertex -2.316958 7.758006 20.741993
    endloop
  endfacet
  facet normal -0.566430 -0.000000 -0.824110
    outer loop
      vertex -2.381678 14.286474 20.786476
      vertex -2.316958 7.758006 20.741993
      vertex -2.381678 7.713526 20.786476
    endloop
  endfacet
  facet normal -0.629313 -0.000000 -0.777152
    outer loop
      vertex -2.381678 14.286474 20.786476
      vertex -2.381678 7.713526 20.786476
      vertex -2.503696 7.614717 20.885283
    endloop
  endfacet
  facet normal -0.629313 -0.000000 -0.777152
    outer loop
      vertex -2.503696 14.385283 20.885283
      vertex -2.381678 14.286474 20.786476
      vertex -2.503696 7.614717 20.885283
    endloop
  endfacet
  facet normal -0.707106 -0.000000 -0.707108
    outer loop
      vertex -2.503696 14.385283 20.885283
      vertex -2.503696 7.614717 20.885283
      vertex -2.614717 7.503696 20.996304
    endloop
  endfacet
  facet normal -0.707106 -0.000000 -0.707108
    outer loop
      vertex -2.614717 14.496305 20.996304
      vertex -2.503696 14.385283 20.885283
      vertex -2.614717 7.503696 20.996304
    endloop
  endfacet
  facet normal -0.777148 -0.000000 -0.629318
    outer loop
      vertex -2.614717 14.496305 20.996304
      vertex -2.614717 7.503696 20.996304
      vertex -2.713526 7.381678 21.118322
    endloop
  endfacet
  facet normal -0.777148 -0.000000 -0.629318
    outer loop
      vertex -2.713526 14.618322 21.118322
      vertex -2.614717 14.496305 20.996304
      vertex -2.713526 7.381678 21.118322
    endloop
  endfacet
  facet normal -0.838670 -0.000000 -0.544640
    outer loop
      vertex -2.713526 14.618322 21.118322
      vertex -2.713526 7.381678 21.118322
      vertex -2.799038 7.250000 21.250000
    endloop
  endfacet
  facet normal -0.838670 -0.000000 -0.544640
    outer loop
      vertex -2.799038 14.750000 21.250000
      vertex -2.713526 14.618322 21.118322
      vertex -2.799038 7.250000 21.250000
    endloop
  endfacet
  facet normal -0.891006 -0.000000 -0.453992
    outer loop
      vertex -2.799038 14.750000 21.250000
      vertex -2.799038 7.250000 21.250000
      vertex -2.870318 7.110105 21.389894
    endloop
  endfacet
  facet normal -0.891006 -0.000000 -0.453992
    outer loop
      vertex -2.870318 14.889895 21.389894
      vertex -2.799038 14.750000 21.250000
      vertex -2.870318 7.110105 21.389894
    endloop
  endfacet
  facet normal -0.933581 -0.000000 -0.358367
    outer loop
      vertex -2.870318 14.889895 21.389894
      vertex -2.870318 7.110105 21.389894
      vertex -2.926585 6.963525 21.536474
    endloop
  endfacet
  facet normal -0.933581 -0.000000 -0.358367
    outer loop
      vertex -2.926585 15.036475 21.536474
      vertex -2.870318 14.889895 21.389894
      vertex -2.926585 6.963525 21.536474
    endloop
  endfacet
  facet normal -0.965925 -0.000000 -0.258821
    outer loop
      vertex -2.926585 15.036475 21.536474
      vertex -2.926585 6.963525 21.536474
      vertex -2.967221 6.811867 21.688131
    endloop
  endfacet
  facet normal -0.965925 -0.000000 -0.258821
    outer loop
      vertex -2.967221 15.188132 21.688131
      vertex -2.926585 15.036475 21.536474
      vertex -2.967221 6.811867 21.688131
    endloop
  endfacet
  facet normal -0.987689 -0.000000 -0.156431
    outer loop
      vertex -2.967221 15.188132 21.688131
      vertex -2.967221 6.811867 21.688131
      vertex -2.991783 6.656793 21.843208
    endloop
  endfacet
  facet normal -0.987689 -0.000000 -0.156431
    outer loop
      vertex -2.991783 15.343207 21.843208
      vertex -2.967221 15.188132 21.688131
      vertex -2.991783 6.656793 21.843208
    endloop
  endfacet
  facet normal -0.998629 -0.000000 -0.052337
    outer loop
      vertex -2.991783 15.343207 21.843208
      vertex -2.991783 6.656793 21.843208
      vertex -3.000000 6.500000 22.000000
    endloop
  endfacet
  facet normal -0.998629 -0.000000 -0.052337
    outer loop
      vertex -3.000000 15.500000 22.000000
      vertex -2.991783 15.343207 21.843208
      vertex -3.000000 6.500000 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 9.250000 -2.000000 -6.000000
      vertex 22.250000 -2.000000 -6.000000
      vertex 22.250000 -1.000000 -6.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 9.250000 -2.000000 -6.000000
      vertex 22.250000 -1.000000 -6.000000
      vertex 9.250000 -1.000000 -6.000000
    endloop
  endfacet
  facet normal -0.998630 -0.052337 0.000000
    outer loop
      vertex -2.991783 15.343207 14.656793
      vertex -3.000000 15.500000 22.000000
      vertex -3.000000 15.500000 14.500000
    endloop
  endfacet
  facet normal -0.998630 -0.052337 -0.000000
    outer loop
      vertex -2.991783 15.343207 21.843208
      vertex -3.000000 15.500000 22.000000
      vertex -2.991783 15.343207 14.656793
    endloop
  endfacet
  facet normal -0.987689 -0.156433 -0.000000
    outer loop
      vertex -2.991783 15.343207 21.843208
      vertex -2.991783 15.343207 14.656793
      vertex -2.967221 15.188132 14.811868
    endloop
  endfacet
  facet normal -0.987689 -0.156433 -0.000000
    outer loop
      vertex -2.967221 15.188132 21.688131
      vertex -2.991783 15.343207 21.843208
      vertex -2.967221 15.188132 14.811868
    endloop
  endfacet
  facet normal -0.965925 -0.258821 -0.000000
    outer loop
      vertex -2.967221 15.188132 21.688131
      vertex -2.967221 15.188132 14.811868
      vertex -2.926585 15.036475 14.963526
    endloop
  endfacet
  facet normal -0.965925 -0.258821 -0.000000
    outer loop
      vertex -2.926585 15.036475 21.536474
      vertex -2.967221 15.188132 21.688131
      vertex -2.926585 15.036475 14.963526
    endloop
  endfacet
  facet normal -0.933581 -0.358367 -0.000000
    outer loop
      vertex -2.926585 15.036475 21.536474
      vertex -2.926585 15.036475 14.963526
      vertex -2.870318 14.889895 15.110106
    endloop
  endfacet
  facet normal -0.933581 -0.358367 -0.000000
    outer loop
      vertex -2.870318 14.889895 21.389894
      vertex -2.926585 15.036475 21.536474
      vertex -2.870318 14.889895 15.110106
    endloop
  endfacet
  facet normal -0.891007 -0.453989 -0.000000
    outer loop
      vertex -2.870318 14.889895 21.389894
      vertex -2.870318 14.889895 15.110106
      vertex -2.799038 14.750000 15.250000
    endloop
  endfacet
  facet normal -0.891007 -0.453989 -0.000000
    outer loop
      vertex -2.799038 14.750000 21.250000
      vertex -2.870318 14.889895 21.389894
      vertex -2.799038 14.750000 15.250000
    endloop
  endfacet
  facet normal -0.838670 -0.544640 -0.000000
    outer loop
      vertex -2.799038 14.750000 21.250000
      vertex -2.799038 14.750000 15.250000
      vertex -2.713526 14.618322 15.381678
    endloop
  endfacet
  facet normal -0.838670 -0.544640 -0.000000
    outer loop
      vertex -2.713526 14.618322 21.118322
      vertex -2.799038 14.750000 21.250000
      vertex -2.713526 14.618322 15.381678
    endloop
  endfacet
  facet normal -0.777145 -0.629321 -0.000000
    outer loop
      vertex -2.713526 14.618322 21.118322
      vertex -2.713526 14.618322 15.381678
      vertex -2.614717 14.496305 15.503696
    endloop
  endfacet
  facet normal -0.777145 -0.629321 -0.000000
    outer loop
      vertex -2.614717 14.496305 20.996304
      vertex -2.713526 14.618322 21.118322
      vertex -2.614717 14.496305 15.503696
    endloop
  endfacet
  facet normal -0.707109 -0.707105 -0.000000
    outer loop
      vertex -2.614717 14.496305 20.996304
      vertex -2.614717 14.496305 15.503696
      vertex -2.503696 14.385283 15.614717
    endloop
  endfacet
  facet normal -0.707109 -0.707105 -0.000000
    outer loop
      vertex -2.503696 14.385283 20.885283
      vertex -2.614717 14.496305 20.996304
      vertex -2.503696 14.385283 15.614717
    endloop
  endfacet
  facet normal -0.629320 -0.777146 -0.000000
    outer loop
      vertex -2.503696 14.385283 20.885283
      vertex -2.503696 14.385283 15.614717
      vertex -2.381678 14.286474 15.713526
    endloop
  endfacet
  facet normal -0.629320 -0.777146 -0.000000
    outer loop
      vertex -2.381678 14.286474 20.786476
      vertex -2.503696 14.385283 20.885283
      vertex -2.381678 14.286474 15.713526
    endloop
  endfacet
  facet normal -0.566405 -0.824127 0.000000
    outer loop
      vertex -2.316958 14.241994 20.741993
      vertex -2.381678 14.286474 20.786476
      vertex -2.381678 14.286474 15.713526
    endloop
  endfacet
  facet normal -0.566405 -0.824127 -0.000000
    outer loop
      vertex -2.316958 14.241994 20.741993
      vertex -2.381678 14.286474 15.713526
      vertex -2.316958 14.241994 15.758006
    endloop
  endfacet
  facet normal -0.522496 -0.852642 0.000000
    outer loop
      vertex -2.250000 14.200962 20.700962
      vertex -2.316958 14.241994 20.741993
      vertex -2.316958 14.241994 15.758006
    endloop
  endfacet
  facet normal -0.522495 -0.852642 -0.000000
    outer loop
      vertex -2.250000 14.200962 20.700962
      vertex -2.316958 14.241994 15.758006
      vertex -2.250000 14.200962 15.799038
    endloop
  endfacet
  facet normal -0.477159 -0.878817 0.000000
    outer loop
      vertex -2.180986 14.163490 20.663490
      vertex -2.250000 14.200962 20.700962
      vertex -2.250000 14.200962 15.799038
    endloop
  endfacet
  facet normal -0.477159 -0.878817 -0.000000
    outer loop
      vertex -2.180986 14.163490 20.663490
      vertex -2.250000 14.200962 15.799038
      vertex -2.180986 14.163490 15.836509
    endloop
  endfacet
  facet normal -0.430515 -0.902583 0.000000
    outer loop
      vertex -2.110105 14.129682 20.629683
      vertex -2.180986 14.163490 20.663490
      vertex -2.180986 14.163490 15.836509
    endloop
  endfacet
  facet normal -0.430515 -0.902583 -0.000000
    outer loop
      vertex -2.110105 14.129682 20.629683
      vertex -2.180986 14.163490 15.836509
      vertex -2.110105 14.129682 15.870317
    endloop
  endfacet
  facet normal -0.382680 -0.923881 0.000000
    outer loop
      vertex -2.037552 14.099629 20.599630
      vertex -2.110105 14.129682 20.629683
      vertex -2.110105 14.129682 15.870317
    endloop
  endfacet
  facet normal -0.382680 -0.923881 -0.000000
    outer loop
      vertex -2.037552 14.099629 20.599630
      vertex -2.110105 14.129682 15.870317
      vertex -2.037552 14.099629 15.900370
    endloop
  endfacet
  facet normal -0.333802 -0.942643 0.000000
    outer loop
      vertex -1.963526 14.073416 20.573416
      vertex -2.037552 14.099629 20.599630
      vertex -2.037552 14.099629 15.900370
    endloop
  endfacet
  facet normal -0.333802 -0.942643 -0.000000
    outer loop
      vertex -1.963526 14.073416 20.573416
      vertex -2.037552 14.099629 15.900370
      vertex -1.963526 14.073416 15.926584
    endloop
  endfacet
  facet normal -0.284022 -0.958818 0.000000
    outer loop
      vertex -1.888229 14.051111 20.551111
      vertex -1.963526 14.073416 20.573416
      vertex -1.963526 14.073416 15.926584
    endloop
  endfacet
  facet normal -0.284022 -0.958818 -0.000000
    outer loop
      vertex -1.888229 14.051111 20.551111
      vertex -1.963526 14.073416 15.926584
      vertex -1.888229 14.051111 15.948888
    endloop
  endfacet
  facet normal -0.233443 -0.972370 0.000000
    outer loop
      vertex -1.811868 14.032779 20.532780
      vertex -1.888229 14.051111 20.551111
      vertex -1.888229 14.051111 15.948888
    endloop
  endfacet
  facet normal -0.233443 -0.972370 -0.000000
    outer loop
      vertex -1.811868 14.032779 20.532780
      vertex -1.888229 14.051111 15.948888
      vertex -1.811868 14.032779 15.967222
    endloop
  endfacet
  facet normal -0.182232 -0.983256 -0.000000
    outer loop
      vertex -1.811868 14.032779 20.532780
      vertex -1.811868 14.032779 15.967222
      vertex -1.734652 14.018468 15.981533
    endloop
  endfacet
  facet normal -0.182232 -0.983256 -0.000000
    outer loop
      vertex -1.734652 14.018468 20.518467
      vertex -1.811868 14.032779 20.532780
      vertex -1.734652 14.018468 15.981533
    endloop
  endfacet
  facet normal -0.130523 -0.991445 -0.000000
    outer loop
      vertex -1.734652 14.018468 20.518467
      vertex -1.734652 14.018468 15.981533
      vertex -1.656793 14.008218 20.508217
    endloop
  endfacet
  facet normal -0.026182 -0.999657 -0.000000
    outer loop
      vertex -1.500000 14.000000 20.500000
      vertex -1.578504 14.002056 15.997945
      vertex -1.500000 14.000000 16.000000
    endloop
  endfacet
  facet normal -0.130523 -0.991445 -0.000000
    outer loop
      vertex -1.656793 14.008218 20.508217
      vertex -1.734652 14.018468 15.981533
      vertex -1.656793 14.008218 15.991783
    endloop
  endfacet
  facet normal -0.078462 -0.996917 -0.000000
    outer loop
      vertex -1.656793 14.008218 20.508217
      vertex -1.656793 14.008218 15.991783
      vertex -1.578504 14.002056 15.997945
    endloop
  endfacet
  facet normal -0.078462 -0.996917 -0.000000
    outer loop
      vertex -1.578504 14.002056 20.502054
      vertex -1.656793 14.008218 20.508217
      vertex -1.578504 14.002056 15.997945
    endloop
  endfacet
  facet normal -0.026182 -0.999657 -0.000000
    outer loop
      vertex -1.578504 14.002056 20.502054
      vertex -1.578504 14.002056 15.997945
      vertex -1.500000 14.000000 20.500000
    endloop
  endfacet
  facet normal -1.000000 0.000000 -0.000000
    outer loop
      vertex 28.000000 0.000000 -6.500000
      vertex 28.000000 0.000000 -10.500000
      vertex 28.000000 -1.000000 -10.500000
    endloop
  endfacet
  facet normal -1.000000 -0.000000 0.000000
    outer loop
      vertex 28.000000 0.000000 -6.500000
      vertex 28.000000 -1.000000 -10.500000
      vertex 28.000000 -1.000000 -6.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 72.000000 22.000000
      vertex -0.200000 72.000000 22.000000
      vertex -0.218704 72.171982 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 72.000000 22.000000
      vertex -0.314514 71.587555 22.000000
      vertex -0.241877 71.744560 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 72.000000 22.000000
      vertex -0.241877 71.744560 22.000000
      vertex -0.204690 71.913506 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.200000 72.000000 22.000000
      vertex -1.000000 72.000000 22.000000
      vertex -0.204690 71.913506 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 72.000000 22.000000
      vertex -0.703889 71.256813 22.000000
      vertex -0.551050 71.337852 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 72.000000 22.000000
      vertex -0.551050 71.337852 22.000000
      vertex -0.419204 71.449837 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.314514 71.587555 22.000000
      vertex -1.000000 72.000000 22.000000
      vertex -0.419204 71.449837 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 72.000000 22.000000
      vertex -1.214023 71.229156 22.000000
      vertex -1.043311 71.201172 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 72.000000 22.000000
      vertex -1.043311 71.201172 22.000000
      vertex -0.870574 71.210541 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.703889 71.256813 22.000000
      vertex -1.000000 72.000000 22.000000
      vertex -0.870574 71.210541 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 72.000000 22.000000
      vertex -1.517909 71.390274 22.000000
      vertex -1.448950 71.337852 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 72.000000 22.000000
      vertex -1.448950 71.337852 22.000000
      vertex -1.374727 71.293190 22.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex -1.214023 71.229156 22.000000
      vertex -1.000000 72.000000 22.000000
      vertex -1.374727 71.293190 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 72.000000 22.000000
      vertex -1.781296 71.828026 22.000000
      vertex -1.726060 71.664085 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 72.000000 22.000000
      vertex -1.726060 71.664085 22.000000
      vertex -1.636874 71.515862 22.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex -1.517909 71.390274 22.000000
      vertex -1.000000 72.000000 22.000000
      vertex -1.636874 71.515862 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 72.000000 22.000000
      vertex -1.726060 72.335915 22.000000
      vertex -1.781296 72.171982 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 72.000000 22.000000
      vertex -1.781296 72.171982 22.000000
      vertex -1.800000 72.000000 22.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex -1.781296 71.828026 22.000000
      vertex -1.000000 72.000000 22.000000
      vertex -1.800000 72.000000 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 72.000000 22.000000
      vertex -1.448950 72.662155 22.000000
      vertex -1.517909 72.609734 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 72.000000 22.000000
      vertex -1.517909 72.609734 22.000000
      vertex -1.636874 72.484146 22.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex -1.726060 72.335915 22.000000
      vertex -1.000000 72.000000 22.000000
      vertex -1.636874 72.484146 22.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex -1.000000 72.000000 22.000000
      vertex -0.956689 72.798828 22.000000
      vertex -1.129426 72.789459 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 72.000000 22.000000
      vertex -1.129426 72.789459 22.000000
      vertex -1.296111 72.743187 22.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex -1.448950 72.662155 22.000000
      vertex -1.000000 72.000000 22.000000
      vertex -1.296111 72.743187 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 72.000000 22.000000
      vertex -0.482091 72.609734 22.000000
      vertex -0.625273 72.706810 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 72.000000 22.000000
      vertex -0.625273 72.706810 22.000000
      vertex -0.785977 72.770844 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.956689 72.798828 22.000000
      vertex -1.000000 72.000000 22.000000
      vertex -0.785977 72.770844 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 72.000000 22.000000
      vertex -0.218704 72.171982 22.000000
      vertex -0.273940 72.335915 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -1.000000 72.000000 22.000000
      vertex -0.273940 72.335915 22.000000
      vertex -0.363126 72.484146 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex -0.482091 72.609734 22.000000
      vertex -1.000000 72.000000 22.000000
      vertex -0.363126 72.484146 22.000000
    endloop
  endfacet
  facet normal -1.000000 0.000000 0.000000
    outer loop
      vertex 2.000000 71.000000 11.000000
      vertex 2.000000 64.500000 11.000000
      vertex 2.000000 64.500000 13.000000
    endloop
  endfacet
  facet normal -1.000000 0.000000 0.000000
    outer loop
      vertex 2.000000 71.000000 11.000000
      vertex 2.000000 64.500000 13.000000
      vertex 2.000000 71.000000 13.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 2.000000 71.000000 11.000000
      vertex 4.378966 68.456261 11.000000
      vertex 4.255834 68.414772 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 2.000000 71.000000 11.000000
      vertex 4.255834 68.414772 11.000000
      vertex 4.137910 68.360214 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 2.000000 71.000000 11.000000
      vertex 4.137910 68.360214 11.000000
      vertex 4.026576 68.293228 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.923136 68.214592 11.000000
      vertex 2.000000 71.000000 11.000000
      vertex 4.026576 68.293228 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 2.000000 71.000000 11.000000
      vertex 3.923136 68.214592 11.000000
      vertex 3.828805 68.125244 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 2.000000 71.000000 11.000000
      vertex 3.828805 68.125244 11.000000
      vertex 3.744688 68.026207 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.671771 67.918663 11.000000
      vertex 2.000000 71.000000 11.000000
      vertex 3.744688 68.026207 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.507034 67.429741 11.000000
      vertex 3.500000 67.300003 11.000000
      vertex 2.000000 64.500000 11.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 3.507034 67.429741 11.000000
      vertex 2.000000 64.500000 11.000000
      vertex 2.000000 71.000000 11.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 3.528055 67.557968 11.000000
      vertex 3.507034 67.429741 11.000000
      vertex 2.000000 71.000000 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 2.000000 64.500000 11.000000
      vertex 3.500000 67.300003 11.000000
      vertex 3.507034 67.170258 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 2.000000 64.500000 11.000000
      vertex 3.507034 67.170258 11.000000
      vertex 3.528055 67.042038 11.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 3.562816 66.916840 11.000000
      vertex 2.000000 64.500000 11.000000
      vertex 3.528055 67.042038 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 2.000000 64.500000 11.000000
      vertex 3.562816 66.916840 11.000000
      vertex 3.610909 66.796135 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 2.000000 64.500000 11.000000
      vertex 3.610909 66.796135 11.000000
      vertex 3.671771 66.681335 11.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 3.744688 66.573792 11.000000
      vertex 2.000000 64.500000 11.000000
      vertex 3.671771 66.681335 11.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 19.271770 66.681335 11.000000
      vertex 19.344688 66.573792 11.000000
      vertex 2.000000 64.500000 11.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 19.271770 66.681335 11.000000
      vertex 2.000000 64.500000 11.000000
      vertex 19.210911 66.796135 11.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 19.737911 66.239792 11.000000
      vertex 2.000000 64.500000 11.000000
      vertex 19.626575 66.306770 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 2.000000 71.000000 11.000000
      vertex 4.894138 68.484192 11.000000
      vertex 4.764966 68.498238 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 2.000000 71.000000 11.000000
      vertex 3.671771 67.918663 11.000000
      vertex 3.610909 67.803864 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 2.000000 71.000000 11.000000
      vertex 3.610909 67.803864 11.000000
      vertex 3.562816 67.683159 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 3.528055 67.557968 11.000000
      vertex 2.000000 71.000000 11.000000
      vertex 3.562816 67.683159 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 2.000000 64.500000 11.000000
      vertex 3.744688 66.573792 11.000000
      vertex 3.828805 66.474754 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 2.000000 64.500000 11.000000
      vertex 3.828805 66.474754 11.000000
      vertex 3.923136 66.385406 11.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 4.026576 66.306770 11.000000
      vertex 2.000000 64.500000 11.000000
      vertex 3.923136 66.385406 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 2.000000 64.500000 11.000000
      vertex 19.344688 66.573792 11.000000
      vertex 19.428804 66.474754 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 2.000000 64.500000 11.000000
      vertex 19.428804 66.474754 11.000000
      vertex 19.523136 66.385406 11.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 19.626575 66.306770 11.000000
      vertex 2.000000 64.500000 11.000000
      vertex 19.523136 66.385406 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 4.894138 66.115814 11.000000
      vertex 19.523136 68.214592 11.000000
      vertex 19.428804 68.125244 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 4.894138 66.115814 11.000000
      vertex 19.428804 68.125244 11.000000
      vertex 19.344688 68.026207 11.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 19.271770 67.918663 11.000000
      vertex 4.894138 66.115814 11.000000
      vertex 19.344688 68.026207 11.000000
    endloop
  endfacet
  facet normal -0.000000 -0.000000 -1.000000
    outer loop
      vertex 20.364965 66.101761 11.000000
      vertex 23.000000 64.500000 11.000000
      vertex 20.235033 66.101761 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 2.000000 71.000000 11.000000
      vertex 4.764966 68.498238 11.000000
      vertex 4.635033 68.498238 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 2.000000 71.000000 11.000000
      vertex 4.635033 68.498238 11.000000
      vertex 4.505862 68.484192 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 4.378966 68.456261 11.000000
      vertex 2.000000 71.000000 11.000000
      vertex 4.505862 68.484192 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 2.000000 64.500000 11.000000
      vertex 4.026576 66.306770 11.000000
      vertex 4.137910 66.239792 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 2.000000 64.500000 11.000000
      vertex 4.137910 66.239792 11.000000
      vertex 4.255834 66.185226 11.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 4.378966 66.143745 11.000000
      vertex 2.000000 64.500000 11.000000
      vertex 4.255834 66.185226 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 4.894138 66.115814 11.000000
      vertex 19.855835 68.414772 11.000000
      vertex 19.737911 68.360214 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 4.894138 66.115814 11.000000
      vertex 19.737911 68.360214 11.000000
      vertex 19.626575 68.293228 11.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 19.523136 68.214592 11.000000
      vertex 4.894138 66.115814 11.000000
      vertex 19.626575 68.293228 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 4.894138 66.115814 11.000000
      vertex 19.271770 67.918663 11.000000
      vertex 19.210911 67.803864 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 4.894138 66.115814 11.000000
      vertex 19.210911 67.803864 11.000000
      vertex 19.162817 67.683159 11.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 19.128056 67.557968 11.000000
      vertex 4.894138 66.115814 11.000000
      vertex 19.162817 67.683159 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.000000 71.000000 11.000000
      vertex 20.621033 68.456261 11.000000
      vertex 20.494139 68.484192 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.000000 71.000000 11.000000
      vertex 20.494139 68.484192 11.000000
      vertex 20.364965 68.498238 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 20.235033 68.498238 11.000000
      vertex 23.000000 71.000000 11.000000
      vertex 20.364965 68.498238 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 2.000000 64.500000 11.000000
      vertex 4.378966 66.143745 11.000000
      vertex 4.505862 66.115814 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 2.000000 64.500000 11.000000
      vertex 4.505862 66.115814 11.000000
      vertex 4.635033 66.101761 11.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 4.764966 66.101761 11.000000
      vertex 2.000000 64.500000 11.000000
      vertex 4.635033 66.101761 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 4.894138 66.115814 11.000000
      vertex 19.128056 67.557968 11.000000
      vertex 19.107035 67.429741 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 4.894138 66.115814 11.000000
      vertex 19.107035 67.429741 11.000000
      vertex 19.099998 67.300003 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 4.764966 66.101761 11.000000
      vertex 4.894138 66.115814 11.000000
      vertex 19.099998 67.300003 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 2.000000 64.500000 11.000000
      vertex 19.737911 66.239792 11.000000
      vertex 19.855835 66.185226 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 2.000000 64.500000 11.000000
      vertex 19.855835 66.185226 11.000000
      vertex 19.978966 66.143745 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.000000 64.500000 11.000000
      vertex 2.000000 64.500000 11.000000
      vertex 19.978966 66.143745 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.000000 64.500000 11.000000
      vertex 19.978966 66.143745 11.000000
      vertex 20.105862 66.115814 11.000000
    endloop
  endfacet
  facet normal -0.000000 -0.000000 -1.000000
    outer loop
      vertex 20.235033 66.101761 11.000000
      vertex 23.000000 64.500000 11.000000
      vertex 20.105862 66.115814 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.000000 64.500000 11.000000
      vertex 20.364965 66.101761 11.000000
      vertex 20.494139 66.115814 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.000000 64.500000 11.000000
      vertex 20.494139 66.115814 11.000000
      vertex 20.621033 66.143745 11.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 20.744165 66.185226 11.000000
      vertex 23.000000 64.500000 11.000000
      vertex 20.621033 66.143745 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.000000 64.500000 11.000000
      vertex 20.744165 66.185226 11.000000
      vertex 20.862089 66.239792 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.000000 64.500000 11.000000
      vertex 20.862089 66.239792 11.000000
      vertex 20.973425 66.306770 11.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 21.076864 66.385406 11.000000
      vertex 23.000000 64.500000 11.000000
      vertex 20.973425 66.306770 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 4.764966 66.101761 11.000000
      vertex 19.099998 67.300003 11.000000
      vertex 19.107035 67.170258 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 4.764966 66.101761 11.000000
      vertex 19.107035 67.170258 11.000000
      vertex 19.128056 67.042038 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 2.000000 64.500000 11.000000
      vertex 4.764966 66.101761 11.000000
      vertex 19.128056 67.042038 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 2.000000 64.500000 11.000000
      vertex 19.128056 67.042038 11.000000
      vertex 19.162817 66.916840 11.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 19.210911 66.796135 11.000000
      vertex 2.000000 64.500000 11.000000
      vertex 19.162817 66.916840 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.000000 71.000000 11.000000
      vertex 21.471945 67.557968 11.000000
      vertex 21.437183 67.683159 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.000000 71.000000 11.000000
      vertex 21.255312 68.026207 11.000000
      vertex 21.171196 68.125244 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.000000 71.000000 11.000000
      vertex 21.171196 68.125244 11.000000
      vertex 21.076864 68.214592 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 20.973425 68.293228 11.000000
      vertex 23.000000 71.000000 11.000000
      vertex 21.076864 68.214592 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.000000 71.000000 11.000000
      vertex 5.476863 68.214592 11.000000
      vertex 5.373425 68.293228 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.000000 64.500000 11.000000
      vertex 21.076864 66.385406 11.000000
      vertex 21.171196 66.474754 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.000000 64.500000 11.000000
      vertex 21.171196 66.474754 11.000000
      vertex 21.255312 66.573792 11.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 21.328230 66.681335 11.000000
      vertex 23.000000 64.500000 11.000000
      vertex 21.255312 66.573792 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.000000 71.000000 11.000000
      vertex 20.973425 68.293228 11.000000
      vertex 20.862089 68.360214 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.000000 71.000000 11.000000
      vertex 20.862089 68.360214 11.000000
      vertex 20.744165 68.414772 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 20.621033 68.456261 11.000000
      vertex 23.000000 71.000000 11.000000
      vertex 20.744165 68.414772 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 20.105862 68.484192 11.000000
      vertex 5.262090 66.239792 11.000000
      vertex 5.373425 66.306770 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 5.571195 68.125244 11.000000
      vertex 5.476863 68.214592 11.000000
      vertex 23.000000 71.000000 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.000000 71.000000 11.000000
      vertex 5.373425 68.293228 11.000000
      vertex 5.262090 68.360214 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.000000 71.000000 11.000000
      vertex 5.262090 68.360214 11.000000
      vertex 5.144166 68.414772 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 2.000000 71.000000 11.000000
      vertex 23.000000 71.000000 11.000000
      vertex 5.144166 68.414772 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 2.000000 71.000000 11.000000
      vertex 5.144166 68.414772 11.000000
      vertex 5.021034 68.456261 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 4.894138 68.484192 11.000000
      vertex 2.000000 71.000000 11.000000
      vertex 5.021034 68.456261 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.000000 64.500000 11.000000
      vertex 21.328230 66.681335 11.000000
      vertex 21.389091 66.796135 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.000000 64.500000 11.000000
      vertex 21.389091 66.796135 11.000000
      vertex 21.437183 66.916840 11.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 21.471945 67.042038 11.000000
      vertex 23.000000 64.500000 11.000000
      vertex 21.437183 66.916840 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.000000 71.000000 11.000000
      vertex 21.437183 67.683159 11.000000
      vertex 21.389091 67.803864 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.000000 71.000000 11.000000
      vertex 21.389091 67.803864 11.000000
      vertex 21.328230 67.918663 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 21.255312 68.026207 11.000000
      vertex 23.000000 71.000000 11.000000
      vertex 21.328230 67.918663 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 19.978966 68.456261 11.000000
      vertex 19.855835 68.414772 11.000000
      vertex 4.894138 66.115814 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 19.978966 68.456261 11.000000
      vertex 4.894138 66.115814 11.000000
      vertex 5.021034 66.143745 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 20.105862 68.484192 11.000000
      vertex 19.978966 68.456261 11.000000
      vertex 5.021034 66.143745 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 20.105862 68.484192 11.000000
      vertex 5.021034 66.143745 11.000000
      vertex 5.144166 66.185226 11.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 5.262090 66.239792 11.000000
      vertex 20.105862 68.484192 11.000000
      vertex 5.144166 66.185226 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 20.105862 68.484192 11.000000
      vertex 5.373425 66.306770 11.000000
      vertex 5.476863 66.385406 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 20.105862 68.484192 11.000000
      vertex 5.476863 66.385406 11.000000
      vertex 5.571195 66.474754 11.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 5.655312 66.573792 11.000000
      vertex 20.105862 68.484192 11.000000
      vertex 5.571195 66.474754 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.000000 71.000000 11.000000
      vertex 5.837184 67.683159 11.000000
      vertex 5.789091 67.803864 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.000000 64.500000 11.000000
      vertex 21.471945 67.042038 11.000000
      vertex 21.492966 67.170258 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.000000 64.500000 11.000000
      vertex 21.492966 67.170258 11.000000
      vertex 21.500000 67.300003 11.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 23.000000 71.000000 11.000000
      vertex 23.000000 64.500000 11.000000
      vertex 21.500000 67.300003 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.000000 71.000000 11.000000
      vertex 21.500000 67.300003 11.000000
      vertex 21.492966 67.429741 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 21.471945 67.557968 11.000000
      vertex 23.000000 71.000000 11.000000
      vertex 21.492966 67.429741 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.000000 71.000000 11.000000
      vertex 5.789091 67.803864 11.000000
      vertex 5.728229 67.918663 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.000000 71.000000 11.000000
      vertex 5.728229 67.918663 11.000000
      vertex 5.655312 68.026207 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 5.571195 68.125244 11.000000
      vertex 23.000000 71.000000 11.000000
      vertex 5.655312 68.026207 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 20.105862 68.484192 11.000000
      vertex 5.900000 67.300003 11.000000
      vertex 5.892965 67.429741 11.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 -1.000000
    outer loop
      vertex 20.105862 68.484192 11.000000
      vertex 5.892965 67.429741 11.000000
      vertex 20.235033 68.498238 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 20.105862 68.484192 11.000000
      vertex 5.655312 66.573792 11.000000
      vertex 5.728229 66.681335 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 20.105862 68.484192 11.000000
      vertex 5.728229 66.681335 11.000000
      vertex 5.789091 66.796135 11.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 5.837184 66.916840 11.000000
      vertex 20.105862 68.484192 11.000000
      vertex 5.789091 66.796135 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 20.105862 68.484192 11.000000
      vertex 5.837184 66.916840 11.000000
      vertex 5.871944 67.042038 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 20.105862 68.484192 11.000000
      vertex 5.871944 67.042038 11.000000
      vertex 5.892965 67.170258 11.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 -1.000000
    outer loop
      vertex 5.900000 67.300003 11.000000
      vertex 20.105862 68.484192 11.000000
      vertex 5.892965 67.170258 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.000000 71.000000 11.000000
      vertex 20.235033 68.498238 11.000000
      vertex 5.892965 67.429741 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 23.000000 71.000000 11.000000
      vertex 5.892965 67.429741 11.000000
      vertex 5.871944 67.557968 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 -1.000000
    outer loop
      vertex 5.837184 67.683159 11.000000
      vertex 23.000000 71.000000 11.000000
      vertex 5.871944 67.557968 11.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 72.000000 22.000000
      vertex 32.799999 72.000000 22.000000
      vertex 32.781296 72.171982 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 72.000000 22.000000
      vertex 32.685486 71.587555 22.000000
      vertex 32.758125 71.744560 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 72.000000 22.000000
      vertex 32.758125 71.744560 22.000000
      vertex 32.795311 71.913506 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.799999 72.000000 22.000000
      vertex 32.000000 72.000000 22.000000
      vertex 32.795311 71.913506 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 72.000000 22.000000
      vertex 32.296108 71.256813 22.000000
      vertex 32.448952 71.337852 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 72.000000 22.000000
      vertex 32.448952 71.337852 22.000000
      vertex 32.580795 71.449837 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.685486 71.587555 22.000000
      vertex 32.000000 72.000000 22.000000
      vertex 32.580795 71.449837 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 72.000000 22.000000
      vertex 31.785976 71.229156 22.000000
      vertex 31.956688 71.201172 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 72.000000 22.000000
      vertex 31.956688 71.201172 22.000000
      vertex 32.129425 71.210541 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.296108 71.256813 22.000000
      vertex 32.000000 72.000000 22.000000
      vertex 32.129425 71.210541 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 72.000000 22.000000
      vertex 31.482090 71.390274 22.000000
      vertex 31.551052 71.337852 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 72.000000 22.000000
      vertex 31.551052 71.337852 22.000000
      vertex 31.625275 71.293190 22.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 31.785976 71.229156 22.000000
      vertex 32.000000 72.000000 22.000000
      vertex 31.625275 71.293190 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 72.000000 22.000000
      vertex 31.218704 71.828026 22.000000
      vertex 31.273939 71.664085 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 72.000000 22.000000
      vertex 31.273939 71.664085 22.000000
      vertex 31.363127 71.515862 22.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 31.482090 71.390274 22.000000
      vertex 32.000000 72.000000 22.000000
      vertex 31.363127 71.515862 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 72.000000 22.000000
      vertex 31.273939 72.335915 22.000000
      vertex 31.218704 72.171982 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 72.000000 22.000000
      vertex 31.218704 72.171982 22.000000
      vertex 31.199999 72.000000 22.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 31.218704 71.828026 22.000000
      vertex 32.000000 72.000000 22.000000
      vertex 31.199999 72.000000 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 72.000000 22.000000
      vertex 31.551052 72.662155 22.000000
      vertex 31.482090 72.609734 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 72.000000 22.000000
      vertex 31.482090 72.609734 22.000000
      vertex 31.363127 72.484146 22.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 31.273939 72.335915 22.000000
      vertex 32.000000 72.000000 22.000000
      vertex 31.363127 72.484146 22.000000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 32.000000 72.000000 22.000000
      vertex 32.043312 72.798828 22.000000
      vertex 31.870573 72.789459 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 72.000000 22.000000
      vertex 31.870573 72.789459 22.000000
      vertex 31.703890 72.743187 22.000000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 31.551052 72.662155 22.000000
      vertex 32.000000 72.000000 22.000000
      vertex 31.703890 72.743187 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 72.000000 22.000000
      vertex 32.517910 72.609734 22.000000
      vertex 32.374729 72.706810 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 72.000000 22.000000
      vertex 32.374729 72.706810 22.000000
      vertex 32.214024 72.770844 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.043312 72.798828 22.000000
      vertex 32.000000 72.000000 22.000000
      vertex 32.214024 72.770844 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 72.000000 22.000000
      vertex 32.781296 72.171982 22.000000
      vertex 32.726059 72.335915 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.000000 72.000000 22.000000
      vertex 32.726059 72.335915 22.000000
      vertex 32.636875 72.484146 22.000000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 32.517910 72.609734 22.000000
      vertex 32.000000 72.000000 22.000000
      vertex 32.636875 72.484146 22.000000
    endloop
  endfacet
  facet normal 1.000000 0.000000 0.000000
    outer loop
      vertex 3.000000 0.000000 -6.500000
      vertex 3.000000 -1.000000 -6.500000
      vertex 3.000000 -1.000000 -10.500000
    endloop
  endfacet
  facet normal 1.000000 0.000000 0.000000
    outer loop
      vertex 3.000000 0.000000 -6.500000
      vertex 3.000000 -1.000000 -10.500000
      vertex 3.000000 0.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 0.000000
    outer loop
      vertex 2.000000 64.500000 11.000000
      vertex 23.000000 64.500000 11.000000
      vertex 23.000000 64.500000 13.000000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 0.000000
    outer loop
      vertex 2.000000 64.500000 11.000000
      vertex 23.000000 64.500000 13.000000
      vertex 2.000000 64.500000 13.000000
    endloop
  endfacet
  facet normal -0.998533 -0.054140 0.000000
    outer loop
      vertex 21.492966 67.429741 11.000000
      vertex 21.500000 67.300003 11.000000
      vertex 21.500000 67.300003 13.000000
    endloop
  endfacet
  facet normal -0.998533 -0.054140 0.000000
    outer loop
      vertex 21.492966 67.429741 11.000000
      vertex 21.500000 67.300003 13.000000
      vertex 21.492966 67.429741 13.000000
    endloop
  endfacet
  facet normal -0.986828 -0.161775 0.000000
    outer loop
      vertex 21.471945 67.557968 11.000000
      vertex 21.492966 67.429741 11.000000
      vertex 21.492966 67.429741 13.000000
    endloop
  endfacet
  facet normal -0.986828 -0.161775 0.000000
    outer loop
      vertex 21.471945 67.557968 11.000000
      vertex 21.492966 67.429741 13.000000
      vertex 21.471945 67.557968 13.000000
    endloop
  endfacet
  facet normal -0.963545 -0.267545 0.000000
    outer loop
      vertex 21.437183 67.683159 11.000000
      vertex 21.471945 67.557968 11.000000
      vertex 21.471945 67.557968 13.000000
    endloop
  endfacet
  facet normal -0.963545 -0.267545 0.000000
    outer loop
      vertex 21.437183 67.683159 11.000000
      vertex 21.471945 67.557968 13.000000
      vertex 21.437183 67.683159 13.000000
    endloop
  endfacet
  facet normal -0.928980 -0.370130 0.000000
    outer loop
      vertex 21.389091 67.803864 11.000000
      vertex 21.437183 67.683159 11.000000
      vertex 21.437183 67.683159 13.000000
    endloop
  endfacet
  facet normal -0.928980 -0.370130 0.000000
    outer loop
      vertex 21.389091 67.803864 11.000000
      vertex 21.437183 67.683159 13.000000
      vertex 21.389091 67.803864 13.000000
    endloop
  endfacet
  facet normal -0.883516 -0.468401 0.000000
    outer loop
      vertex 21.328230 67.918663 11.000000
      vertex 21.389091 67.803864 11.000000
      vertex 21.389091 67.803864 13.000000
    endloop
  endfacet
  facet normal -0.883516 -0.468401 0.000000
    outer loop
      vertex 21.328230 67.918663 11.000000
      vertex 21.389091 67.803864 13.000000
      vertex 21.328230 67.918663 13.000000
    endloop
  endfacet
  facet normal -0.827684 -0.561194 0.000000
    outer loop
      vertex 21.255312 68.026207 11.000000
      vertex 21.328230 67.918663 11.000000
      vertex 21.328230 67.918663 13.000000
    endloop
  endfacet
  facet normal -0.827684 -0.561194 0.000000
    outer loop
      vertex 21.255312 68.026207 11.000000
      vertex 21.328230 67.918663 13.000000
      vertex 21.255312 68.026207 13.000000
    endloop
  endfacet
  facet normal -0.762188 -0.647355 0.000000
    outer loop
      vertex 21.171196 68.125244 11.000000
      vertex 21.255312 68.026207 11.000000
      vertex 21.255312 68.026207 13.000000
    endloop
  endfacet
  facet normal -0.762188 -0.647355 0.000000
    outer loop
      vertex 21.171196 68.125244 11.000000
      vertex 21.255312 68.026207 13.000000
      vertex 21.171196 68.125244 13.000000
    endloop
  endfacet
  facet normal -0.687667 -0.726026 0.000000
    outer loop
      vertex 21.076864 68.214592 11.000000
      vertex 21.171196 68.125244 11.000000
      vertex 21.171196 68.125244 13.000000
    endloop
  endfacet
  facet normal -0.687667 -0.726026 0.000000
    outer loop
      vertex 21.076864 68.214592 11.000000
      vertex 21.171196 68.125244 13.000000
      vertex 21.076864 68.214592 13.000000
    endloop
  endfacet
  facet normal -0.605192 -0.796080 0.000000
    outer loop
      vertex 20.973425 68.293228 11.000000
      vertex 21.076864 68.214592 11.000000
      vertex 21.076864 68.214592 13.000000
    endloop
  endfacet
  facet normal -0.605192 -0.796080 0.000000
    outer loop
      vertex 20.973425 68.293228 11.000000
      vertex 21.076864 68.214592 13.000000
      vertex 20.973425 68.293228 13.000000
    endloop
  endfacet
  facet normal -0.515540 -0.856865 0.000000
    outer loop
      vertex 20.862089 68.360214 11.000000
      vertex 20.973425 68.293228 11.000000
      vertex 20.973425 68.293228 13.000000
    endloop
  endfacet
  facet normal -0.515540 -0.856865 0.000000
    outer loop
      vertex 20.862089 68.360214 11.000000
      vertex 20.973425 68.293228 13.000000
      vertex 20.862089 68.360214 13.000000
    endloop
  endfacet
  facet normal -0.419892 -0.907574 0.000000
    outer loop
      vertex 20.744165 68.414772 11.000000
      vertex 20.862089 68.360214 11.000000
      vertex 20.862089 68.360214 13.000000
    endloop
  endfacet
  facet normal -0.419892 -0.907574 0.000000
    outer loop
      vertex 20.744165 68.414772 11.000000
      vertex 20.862089 68.360214 13.000000
      vertex 20.744165 68.414772 13.000000
    endloop
  endfacet
  facet normal -0.319304 -0.947652 0.000000
    outer loop
      vertex 20.621033 68.456261 11.000000
      vertex 20.744165 68.414772 11.000000
      vertex 20.744165 68.414772 13.000000
    endloop
  endfacet
  facet normal -0.319304 -0.947652 0.000000
    outer loop
      vertex 20.621033 68.456261 11.000000
      vertex 20.744165 68.414772 13.000000
      vertex 20.621033 68.456261 13.000000
    endloop
  endfacet
  facet normal -0.214968 -0.976621 0.000000
    outer loop
      vertex 20.494139 68.484192 11.000000
      vertex 20.621033 68.456261 11.000000
      vertex 20.621033 68.456261 13.000000
    endloop
  endfacet
  facet normal -0.214968 -0.976621 0.000000
    outer loop
      vertex 20.494139 68.484192 11.000000
      vertex 20.621033 68.456261 13.000000
      vertex 20.494139 68.484192 13.000000
    endloop
  endfacet
  facet normal -0.108098 -0.994140 0.000000
    outer loop
      vertex 20.364965 68.498238 11.000000
      vertex 20.494139 68.484192 11.000000
      vertex 20.494139 68.484192 13.000000
    endloop
  endfacet
  facet normal -0.108098 -0.994140 0.000000
    outer loop
      vertex 20.364965 68.498238 11.000000
      vertex 20.494139 68.484192 13.000000
      vertex 20.364965 68.498238 13.000000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 0.000000
    outer loop
      vertex 20.235033 68.498238 11.000000
      vertex 20.364965 68.498238 11.000000
      vertex 20.364965 68.498238 13.000000
    endloop
  endfacet
  facet normal 0.000000 -1.000000 0.000000
    outer loop
      vertex 20.235033 68.498238 11.000000
      vertex 20.364965 68.498238 13.000000
      vertex 20.235033 68.498238 13.000000
    endloop
  endfacet
  facet normal 0.108100 -0.994140 0.000000
    outer loop
      vertex 20.105862 68.484192 11.000000
      vertex 20.235033 68.498238 11.000000
      vertex 20.235033 68.498238 13.000000
    endloop
  endfacet
  facet normal 0.108100 -0.994140 0.000000
    outer loop
      vertex 20.105862 68.484192 11.000000
      vertex 20.235033 68.498238 13.000000
      vertex 20.105862 68.484192 13.000000
    endloop
  endfacet
  facet normal 0.214965 -0.976622 0.000000
    outer loop
      vertex 19.978966 68.456261 11.000000
      vertex 20.105862 68.484192 11.000000
      vertex 20.105862 68.484192 13.000000
    endloop
  endfacet
  facet normal 0.214965 -0.976622 0.000000
    outer loop
      vertex 19.978966 68.456261 11.000000
      vertex 20.105862 68.484192 13.000000
      vertex 19.978966 68.456261 13.000000
    endloop
  endfacet
  facet normal 0.319309 -0.947651 0.000000
    outer loop
      vertex 19.855835 68.414772 11.000000
      vertex 19.978966 68.456261 11.000000
      vertex 19.978966 68.456261 13.000000
    endloop
  endfacet
  facet normal 0.319309 -0.947651 0.000000
    outer loop
      vertex 19.855835 68.414772 11.000000
      vertex 19.978966 68.456261 13.000000
      vertex 19.855835 68.414772 13.000000
    endloop
  endfacet
  facet normal 0.419892 -0.907574 0.000000
    outer loop
      vertex 19.737911 68.360214 11.000000
      vertex 19.855835 68.414772 11.000000
      vertex 19.855835 68.414772 13.000000
    endloop
  endfacet
  facet normal 0.419892 -0.907574 0.000000
    outer loop
      vertex 19.737911 68.360214 11.000000
      vertex 19.855835 68.414772 13.000000
      vertex 19.737911 68.360214 13.000000
    endloop
  endfacet
  facet normal 0.515540 -0.856865 0.000000
    outer loop
      vertex 19.626575 68.293228 11.000000
      vertex 19.737911 68.360214 11.000000
      vertex 19.737911 68.360214 13.000000
    endloop
  endfacet
  facet normal 0.515540 -0.856865 0.000000
    outer loop
      vertex 19.626575 68.293228 11.000000
      vertex 19.737911 68.360214 13.000000
      vertex 19.626575 68.293228 13.000000
    endloop
  endfacet
  facet normal 0.605192 -0.796080 0.000000
    outer loop
      vertex 19.523136 68.214592 11.000000
      vertex 19.626575 68.293228 11.000000
      vertex 19.626575 68.293228 13.000000
    endloop
  endfacet
  facet normal 0.605192 -0.796080 0.000000
    outer loop
      vertex 19.523136 68.214592 11.000000
      vertex 19.626575 68.293228 13.000000
      vertex 19.523136 68.214592 13.000000
    endloop
  endfacet
  facet normal 0.687667 -0.726026 0.000000
    outer loop
      vertex 19.428804 68.125244 11.000000
      vertex 19.523136 68.214592 11.000000
      vertex 19.523136 68.214592 13.000000
    endloop
  endfacet
  facet normal 0.687667 -0.726026 0.000000
    outer loop
      vertex 19.428804 68.125244 11.000000
      vertex 19.523136 68.214592 13.000000
      vertex 19.428804 68.125244 13.000000
    endloop
  endfacet
  facet normal 0.762188 -0.647355 0.000000
    outer loop
      vertex 19.344688 68.026207 11.000000
      vertex 19.428804 68.125244 11.000000
      vertex 19.428804 68.125244 13.000000
    endloop
  endfacet
  facet normal 0.762188 -0.647355 0.000000
    outer loop
      vertex 19.344688 68.026207 11.000000
      vertex 19.428804 68.125244 13.000000
      vertex 19.344688 68.026207 13.000000
    endloop
  endfacet
  facet normal 0.827684 -0.561194 0.000000
    outer loop
      vertex 19.271770 67.918663 11.000000
      vertex 19.344688 68.026207 11.000000
      vertex 19.344688 68.026207 13.000000
    endloop
  endfacet
  facet normal 0.827684 -0.561194 0.000000
    outer loop
      vertex 19.271770 67.918663 11.000000
      vertex 19.344688 68.026207 13.000000
      vertex 19.271770 67.918663 13.000000
    endloop
  endfacet
  facet normal 0.883522 -0.468389 0.000000
    outer loop
      vertex 19.210911 67.803864 11.000000
      vertex 19.271770 67.918663 11.000000
      vertex 19.271770 67.918663 13.000000
    endloop
  endfacet
  facet normal 0.883522 -0.468389 0.000000
    outer loop
      vertex 19.210911 67.803864 11.000000
      vertex 19.271770 67.918663 13.000000
      vertex 19.210911 67.803864 13.000000
    endloop
  endfacet
  facet normal 0.928975 -0.370143 0.000000
    outer loop
      vertex 19.162817 67.683159 11.000000
      vertex 19.210911 67.803864 11.000000
      vertex 19.210911 67.803864 13.000000
    endloop
  endfacet
  facet normal 0.928975 -0.370143 0.000000
    outer loop
      vertex 19.162817 67.683159 11.000000
      vertex 19.210911 67.803864 13.000000
      vertex 19.162817 67.683159 13.000000
    endloop
  endfacet
  facet normal 0.963545 -0.267545 0.000000
    outer loop
      vertex 19.128056 67.557968 11.000000
      vertex 19.162817 67.683159 11.000000
      vertex 19.162817 67.683159 13.000000
    endloop
  endfacet
  facet normal 0.963545 -0.267545 0.000000
    outer loop
      vertex 19.128056 67.557968 11.000000
      vertex 19.162817 67.683159 13.000000
      vertex 19.128056 67.557968 13.000000
    endloop
  endfacet
  facet normal 0.986828 -0.161775 0.000000
    outer loop
      vertex 19.107035 67.429741 11.000000
      vertex 19.128056 67.557968 11.000000
      vertex 19.128056 67.557968 13.000000
    endloop
  endfacet
  facet normal 0.986828 -0.161775 0.000000
    outer loop
      vertex 19.107035 67.429741 11.000000
      vertex 19.128056 67.557968 13.000000
      vertex 19.107035 67.429741 13.000000
    endloop
  endfacet
  facet normal 0.998533 -0.054154 0.000000
    outer loop
      vertex 19.099998 67.300003 11.000000
      vertex 19.107035 67.429741 11.000000
      vertex 19.107035 67.429741 13.000000
    endloop
  endfacet
  facet normal 0.998533 -0.054154 0.000000
    outer loop
      vertex 19.099998 67.300003 11.000000
      vertex 19.107035 67.429741 13.000000
      vertex 19.099998 67.300003 13.000000
    endloop
  endfacet
  facet normal 0.998533 0.054151 0.000000
    outer loop
      vertex 19.107035 67.170258 11.000000
      vertex 19.099998 67.300003 11.000000
      vertex 19.099998 67.300003 13.000000
    endloop
  endfacet
  facet normal 0.998533 0.054151 -0.000000
    outer loop
      vertex 19.107035 67.170258 11.000000
      vertex 19.099998 67.300003 13.000000
      vertex 19.107035 67.170258 13.000000
    endloop
  endfacet
  facet normal 0.986826 0.161785 0.000000
    outer loop
      vertex 19.128056 67.042038 11.000000
      vertex 19.107035 67.170258 11.000000
      vertex 19.107035 67.170258 13.000000
    endloop
  endfacet
  facet normal 0.986826 0.161785 -0.000000
    outer loop
      vertex 19.128056 67.042038 11.000000
      vertex 19.107035 67.170258 13.000000
      vertex 19.128056 67.042038 13.000000
    endloop
  endfacet
  facet normal 0.963549 0.267530 0.000000
    outer loop
      vertex 19.162817 66.916840 11.000000
      vertex 19.128056 67.042038 11.000000
      vertex 19.128056 67.042038 13.000000
    endloop
  endfacet
  facet normal 0.963549 0.267530 -0.000000
    outer loop
      vertex 19.162817 66.916840 11.000000
      vertex 19.128056 67.042038 13.000000
      vertex 19.162817 66.916840 13.000000
    endloop
  endfacet
  facet normal 0.928975 0.370143 0.000000
    outer loop
      vertex 19.210911 66.796135 11.000000
      vertex 19.162817 66.916840 11.000000
      vertex 19.162817 66.916840 13.000000
    endloop
  endfacet
  facet normal 0.928975 0.370143 -0.000000
    outer loop
      vertex 19.210911 66.796135 11.000000
      vertex 19.162817 66.916840 13.000000
      vertex 19.210911 66.796135 13.000000
    endloop
  endfacet
  facet normal 0.883522 0.468389 0.000000
    outer loop
      vertex 19.271770 66.681335 11.000000
      vertex 19.210911 66.796135 11.000000
      vertex 19.210911 66.796135 13.000000
    endloop
  endfacet
  facet normal 0.883522 0.468389 -0.000000
    outer loop
      vertex 19.271770 66.681335 11.000000
      vertex 19.210911 66.796135 13.000000
      vertex 19.271770 66.681335 13.000000
    endloop
  endfacet
  facet normal 0.827684 0.561194 0.000000
    outer loop
      vertex 19.344688 66.573792 11.000000
      vertex 19.271770 66.681335 11.000000
      vertex 19.271770 66.681335 13.000000
    endloop
  endfacet
  facet normal 0.827684 0.561194 -0.000000
    outer loop
      vertex 19.344688 66.573792 11.000000
      vertex 19.271770 66.681335 13.000000
      vertex 19.344688 66.573792 13.000000
    endloop
  endfacet
  facet normal 0.762188 0.647355 0.000000
    outer loop
      vertex 19.428804 66.474754 11.000000
      vertex 19.344688 66.573792 11.000000
      vertex 19.344688 66.573792 13.000000
    endloop
  endfacet
  facet normal 0.762188 0.647355 -0.000000
    outer loop
      vertex 19.428804 66.474754 11.000000
      vertex 19.344688 66.573792 13.000000
      vertex 19.428804 66.474754 13.000000
    endloop
  endfacet
  facet normal 0.687667 0.726026 0.000000
    outer loop
      vertex 19.523136 66.385406 11.000000
      vertex 19.428804 66.474754 11.000000
      vertex 19.428804 66.474754 13.000000
    endloop
  endfacet
  facet normal 0.687667 0.726026 -0.000000
    outer loop
      vertex 19.523136 66.385406 11.000000
      vertex 19.428804 66.474754 13.000000
      vertex 19.523136 66.385406 13.000000
    endloop
  endfacet
  facet normal 0.605192 0.796080 0.000000
    outer loop
      vertex 19.626575 66.306770 11.000000
      vertex 19.523136 66.385406 11.000000
      vertex 19.523136 66.385406 13.000000
    endloop
  endfacet
  facet normal 0.605192 0.796080 -0.000000
    outer loop
      vertex 19.626575 66.306770 11.000000
      vertex 19.523136 66.385406 13.000000
      vertex 19.626575 66.306770 13.000000
    endloop
  endfacet
  facet normal 0.515497 0.856891 0.000000
    outer loop
      vertex 19.737911 66.239792 11.000000
      vertex 19.626575 66.306770 11.000000
      vertex 19.626575 66.306770 13.000000
    endloop
  endfacet
  facet normal 0.515497 0.856891 -0.000000
    outer loop
      vertex 19.737911 66.239792 11.000000
      vertex 19.626575 66.306770 13.000000
      vertex 19.737911 66.239792 13.000000
    endloop
  endfacet
  facet normal 0.419940 0.907552 0.000000
    outer loop
      vertex 19.855835 66.185226 11.000000
      vertex 19.737911 66.239792 11.000000
      vertex 19.737911 66.239792 13.000000
    endloop
  endfacet
  facet normal 0.419940 0.907552 -0.000000
    outer loop
      vertex 19.855835 66.185226 11.000000
      vertex 19.737911 66.239792 13.000000
      vertex 19.855835 66.185226 13.000000
    endloop
  endfacet
  facet normal 0.319256 0.947668 0.000000
    outer loop
      vertex 19.978966 66.143745 11.000000
      vertex 19.855835 66.185226 11.000000
      vertex 19.855835 66.185226 13.000000
    endloop
  endfacet
  facet normal 0.319256 0.947668 -0.000000
    outer loop
      vertex 19.978966 66.143745 11.000000
      vertex 19.855835 66.185226 13.000000
      vertex 19.978966 66.143745 13.000000
    endloop
  endfacet
  facet normal 0.214965 0.976622 0.000000
    outer loop
      vertex 20.105862 66.115814 11.000000
      vertex 19.978966 66.143745 11.000000
      vertex 19.978966 66.143745 13.000000
    endloop
  endfacet
  facet normal 0.214965 0.976622 -0.000000
    outer loop
      vertex 20.105862 66.115814 11.000000
      vertex 19.978966 66.143745 13.000000
      vertex 20.105862 66.115814 13.000000
    endloop
  endfacet
  facet normal 0.108158 0.994134 0.000000
    outer loop
      vertex 20.235033 66.101761 11.000000
      vertex 20.105862 66.115814 11.000000
      vertex 20.105862 66.115814 13.000000
    endloop
  endfacet
  facet normal 0.108158 0.994134 -0.000000
    outer loop
      vertex 20.235033 66.101761 11.000000
      vertex 20.105862 66.115814 13.000000
      vertex 20.235033 66.101761 13.000000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 20.364965 66.101761 11.000000
      vertex 20.235033 66.101761 11.000000
      vertex 20.235033 66.101761 13.000000
    endloop
  endfacet
  facet normal 0.000000 1.000000 -0.000000
    outer loop
      vertex 20.364965 66.101761 11.000000
      vertex 20.235033 66.101761 13.000000
      vertex 20.364965 66.101761 13.000000
    endloop
  endfacet
  facet normal -0.108156 0.994134 0.000000
    outer loop
      vertex 20.494139 66.115814 11.000000
      vertex 20.364965 66.101761 11.000000
      vertex 20.364965 66.101761 13.000000
    endloop
  endfacet
  facet normal -0.108156 0.994134 0.000000
    outer loop
      vertex 20.494139 66.115814 11.000000
      vertex 20.364965 66.101761 13.000000
      vertex 20.494139 66.115814 13.000000
    endloop
  endfacet
  facet normal -0.214968 0.976621 0.000000
    outer loop
      vertex 20.621033 66.143745 11.000000
      vertex 20.494139 66.115814 11.000000
      vertex 20.494139 66.115814 13.000000
    endloop
  endfacet
  facet normal -0.214968 0.976621 0.000000
    outer loop
      vertex 20.621033 66.143745 11.000000
      vertex 20.494139 66.115814 13.000000
      vertex 20.621033 66.143745 13.000000
    endloop
  endfacet
  facet normal -0.319252 0.947670 0.000000
    outer loop
      vertex 20.744165 66.185226 11.000000
      vertex 20.621033 66.143745 11.000000
      vertex 20.621033 66.143745 13.000000
    endloop
  endfacet
  facet normal -0.319252 0.947670 0.000000
    outer loop
      vertex 20.744165 66.185226 11.000000
      vertex 20.621033 66.143745 13.000000
      vertex 20.744165 66.185226 13.000000
    endloop
  endfacet
  facet normal -0.419940 0.907552 0.000000
    outer loop
      vertex 20.862089 66.239792 11.000000
      vertex 20.744165 66.185226 11.000000
      vertex 20.744165 66.185226 13.000000
    endloop
  endfacet
  facet normal -0.419940 0.907552 0.000000
    outer loop
      vertex 20.862089 66.239792 11.000000
      vertex 20.744165 66.185226 13.000000
      vertex 20.862089 66.239792 13.000000
    endloop
  endfacet
  facet normal -0.515497 0.856891 0.000000
    outer loop
      vertex 20.973425 66.306770 11.000000
      vertex 20.862089 66.239792 11.000000
      vertex 20.862089 66.239792 13.000000
    endloop
  endfacet
  facet normal -0.515497 0.856891 0.000000
    outer loop
      vertex 20.973425 66.306770 11.000000
      vertex 20.862089 66.239792 13.000000
      vertex 20.973425 66.306770 13.000000
    endloop
  endfacet
  facet normal -0.605192 0.796080 0.000000
    outer loop
      vertex 21.076864 66.385406 11.000000
      vertex 20.973425 66.306770 11.000000
      vertex 20.973425 66.306770 13.000000
    endloop
  endfacet
  facet normal -0.605192 0.796080 0.000000
    outer loop
      vertex 21.076864 66.385406 11.000000
      vertex 20.973425 66.306770 13.000000
      vertex 21.076864 66.385406 13.000000
    endloop
  endfacet
  facet normal -0.687667 0.726026 0.000000
    outer loop
      vertex 21.171196 66.474754 11.000000
      vertex 21.076864 66.385406 11.000000
      vertex 21.076864 66.385406 13.000000
    endloop
  endfacet
  facet normal -0.687667 0.726026 0.000000
    outer loop
      vertex 21.171196 66.474754 11.000000
      vertex 21.076864 66.385406 13.000000
      vertex 21.171196 66.474754 13.000000
    endloop
  endfacet
  facet normal -0.762188 0.647355 0.000000
    outer loop
      vertex 21.255312 66.573792 11.000000
      vertex 21.171196 66.474754 11.000000
      vertex 21.171196 66.474754 13.000000
    endloop
  endfacet
  facet normal -0.762188 0.647355 0.000000
    outer loop
      vertex 21.255312 66.573792 11.000000
      vertex 21.171196 66.474754 13.000000
      vertex 21.255312 66.573792 13.000000
    endloop
  endfacet
  facet normal -0.827684 0.561194 0.000000
    outer loop
      vertex 21.328230 66.681335 11.000000
      vertex 21.255312 66.573792 11.000000
      vertex 21.255312 66.573792 13.000000
    endloop
  endfacet
  facet normal -0.827684 0.561194 0.000000
    outer loop
      vertex 21.328230 66.681335 11.000000
      vertex 21.255312 66.573792 13.000000
      vertex 21.328230 66.681335 13.000000
    endloop
  endfacet
  facet normal -0.883516 0.468401 0.000000
    outer loop
      vertex 21.389091 66.796135 11.000000
      vertex 21.328230 66.681335 11.000000
      vertex 21.328230 66.681335 13.000000
    endloop
  endfacet
  facet normal -0.883516 0.468401 0.000000
    outer loop
      vertex 21.389091 66.796135 11.000000
      vertex 21.328230 66.681335 13.000000
      vertex 21.389091 66.796135 13.000000
    endloop
  endfacet
  facet normal -0.928980 0.370130 0.000000
    outer loop
      vertex 21.437183 66.916840 11.000000
      vertex 21.389091 66.796135 11.000000
      vertex 21.389091 66.796135 13.000000
    endloop
  endfacet
  facet normal -0.928980 0.370130 0.000000
    outer loop
      vertex 21.437183 66.916840 11.000000
      vertex 21.389091 66.796135 13.000000
      vertex 21.437183 66.916840 13.000000
    endloop
  endfacet
  facet normal -0.963549 0.267530 0.000000
    outer loop
      vertex 21.471945 67.042038 11.000000
      vertex 21.437183 66.916840 11.000000
      vertex 21.437183 66.916840 13.000000
    endloop
  endfacet
  facet normal -0.963549 0.267530 0.000000
    outer loop
      vertex 21.471945 67.042038 11.000000
      vertex 21.437183 66.916840 13.000000
      vertex 21.471945 67.042038 13.000000
    endloop
  endfacet
  facet normal -0.986826 0.161785 0.000000
    outer loop
      vertex 21.492966 67.170258 11.000000
      vertex 21.471945 67.042038 11.000000
      vertex 21.471945 67.042038 13.000000
    endloop
  endfacet
  facet normal -0.986826 0.161785 0.000000
    outer loop
      vertex 21.492966 67.170258 11.000000
      vertex 21.471945 67.042038 13.000000
      vertex 21.492966 67.170258 13.000000
    endloop
  endfacet
  facet normal -0.998534 0.054137 0.000000
    outer loop
      vertex 21.500000 67.300003 11.000000
      vertex 21.492966 67.170258 11.000000
      vertex 21.492966 67.170258 13.000000
    endloop
  endfacet
  facet normal -0.998534 0.054137 0.000000
    outer loop
      vertex 21.500000 67.300003 11.000000
      vertex 21.492966 67.170258 13.000000
      vertex 21.500000 67.300003 13.000000
    endloop
  endfacet
  facet normal 0.052334 0.998630 0.000000
    outer loop
      vertex 32.209057 73.989044 23.000000
      vertex 32.000000 74.000000 -10.500000
      vertex 32.000000 74.000000 23.000000
    endloop
  endfacet
  facet normal 0.052334 0.998630 -0.000000
    outer loop
      vertex 32.209057 73.989044 -10.500000
      vertex 32.000000 74.000000 -10.500000
      vertex 32.209057 73.989044 23.000000
    endloop
  endfacet
  facet normal 0.156421 0.987691 -0.000000
    outer loop
      vertex 32.209057 73.989044 -10.500000
      vertex 32.209057 73.989044 23.000000
      vertex 32.415821 73.956299 23.000000
    endloop
  endfacet
  facet normal 0.156421 0.987691 -0.000000
    outer loop
      vertex 32.415821 73.956299 -10.500000
      vertex 32.209057 73.989044 -10.500000
      vertex 32.415821 73.956299 23.000000
    endloop
  endfacet
  facet normal 0.258824 0.965925 -0.000000
    outer loop
      vertex 32.415821 73.956299 -10.500000
      vertex 32.415821 73.956299 23.000000
      vertex 32.618034 73.902115 23.000000
    endloop
  endfacet
  facet normal 0.258824 0.965925 -0.000000
    outer loop
      vertex 32.618034 73.902115 -10.500000
      vertex 32.415821 73.956299 -10.500000
      vertex 32.618034 73.902115 23.000000
    endloop
  endfacet
  facet normal 0.358392 0.933571 -0.000000
    outer loop
      vertex 32.618034 73.902115 -10.500000
      vertex 32.618034 73.902115 23.000000
      vertex 32.813473 73.827087 23.000000
    endloop
  endfacet
  facet normal 0.358392 0.933571 -0.000000
    outer loop
      vertex 32.813473 73.827087 -10.500000
      vertex 32.618034 73.902115 -10.500000
      vertex 32.813473 73.827087 23.000000
    endloop
  endfacet
  facet normal 0.453987 0.891008 -0.000000
    outer loop
      vertex 32.813473 73.827087 -10.500000
      vertex 32.813473 73.827087 23.000000
      vertex 33.000000 73.732048 23.000000
    endloop
  endfacet
  facet normal 0.453987 0.891008 -0.000000
    outer loop
      vertex 33.000000 73.732048 -10.500000
      vertex 32.813473 73.827087 -10.500000
      vertex 33.000000 73.732048 23.000000
    endloop
  endfacet
  facet normal 0.544635 0.838673 -0.000000
    outer loop
      vertex 33.000000 73.732048 -10.500000
      vertex 33.000000 73.732048 23.000000
      vertex 33.175568 73.618034 23.000000
    endloop
  endfacet
  facet normal 0.544635 0.838673 -0.000000
    outer loop
      vertex 33.175568 73.618034 -10.500000
      vertex 33.000000 73.732048 -10.500000
      vertex 33.175568 73.618034 23.000000
    endloop
  endfacet
  facet normal 0.629315 0.777150 -0.000000
    outer loop
      vertex 33.175568 73.618034 -10.500000
      vertex 33.175568 73.618034 23.000000
      vertex 33.338261 73.486290 23.000000
    endloop
  endfacet
  facet normal 0.629315 0.777150 -0.000000
    outer loop
      vertex 33.338261 73.486290 -10.500000
      vertex 33.175568 73.618034 -10.500000
      vertex 33.338261 73.486290 23.000000
    endloop
  endfacet
  facet normal 0.707107 0.707107 -0.000000
    outer loop
      vertex 33.338261 73.486290 -10.500000
      vertex 33.338261 73.486290 23.000000
      vertex 33.486286 73.338264 23.000000
    endloop
  endfacet
  facet normal 0.707107 0.707107 -0.000000
    outer loop
      vertex 33.486286 73.338264 -10.500000
      vertex 33.338261 73.486290 -10.500000
      vertex 33.486286 73.338264 23.000000
    endloop
  endfacet
  facet normal 0.777134 0.629335 -0.000000
    outer loop
      vertex 33.486286 73.338264 -10.500000
      vertex 33.486286 73.338264 23.000000
      vertex 33.618034 73.175575 23.000000
    endloop
  endfacet
  facet normal 0.777134 0.629335 -0.000000
    outer loop
      vertex 33.618034 73.175575 -10.500000
      vertex 33.486286 73.338264 -10.500000
      vertex 33.618034 73.175575 23.000000
    endloop
  endfacet
  facet normal 0.838684 0.544618 -0.000000
    outer loop
      vertex 33.618034 73.175575 -10.500000
      vertex 33.618034 73.175575 23.000000
      vertex 33.732048 73.000000 23.000000
    endloop
  endfacet
  facet normal 0.838684 0.544618 -0.000000
    outer loop
      vertex 33.732048 73.000000 -10.500000
      vertex 33.618034 73.175575 -10.500000
      vertex 33.732048 73.000000 23.000000
    endloop
  endfacet
  facet normal 0.890997 0.454008 -0.000000
    outer loop
      vertex 33.732048 73.000000 -10.500000
      vertex 33.732048 73.000000 23.000000
      vertex 33.827091 72.813477 23.000000
    endloop
  endfacet
  facet normal 0.890997 0.454008 -0.000000
    outer loop
      vertex 33.827091 72.813477 -10.500000
      vertex 33.732048 73.000000 -10.500000
      vertex 33.827091 72.813477 23.000000
    endloop
  endfacet
  facet normal 0.933586 0.358354 -0.000000
    outer loop
      vertex 33.827091 72.813477 -10.500000
      vertex 33.827091 72.813477 23.000000
      vertex 33.902111 72.618034 23.000000
    endloop
  endfacet
  facet normal 0.933586 0.358354 -0.000000
    outer loop
      vertex 33.902111 72.618034 -10.500000
      vertex 33.827091 72.813477 -10.500000
      vertex 33.902111 72.618034 23.000000
    endloop
  endfacet
  facet normal 0.965923 0.258828 -0.000000
    outer loop
      vertex 33.902111 72.618034 -10.500000
      vertex 33.902111 72.618034 23.000000
      vertex 33.956295 72.415825 23.000000
    endloop
  endfacet
  facet normal 0.965923 0.258828 -0.000000
    outer loop
      vertex 33.956295 72.415825 -10.500000
      vertex 33.902111 72.618034 -10.500000
      vertex 33.956295 72.415825 23.000000
    endloop
  endfacet
  facet normal 0.987691 0.156421 -0.000000
    outer loop
      vertex 33.956295 72.415825 -10.500000
      vertex 33.956295 72.415825 23.000000
      vertex 33.989040 72.209061 23.000000
    endloop
  endfacet
  facet normal 0.987691 0.156421 -0.000000
    outer loop
      vertex 33.989040 72.209061 -10.500000
      vertex 33.956295 72.415825 -10.500000
      vertex 33.989040 72.209061 23.000000
    endloop
  endfacet
  facet normal 0.998629 0.052351 -0.000000
    outer loop
      vertex 33.989040 72.209061 -10.500000
      vertex 33.989040 72.209061 23.000000
      vertex 34.000000 72.000000 23.000000
    endloop
  endfacet
  facet normal 0.998629 0.052351 -0.000000
    outer loop
      vertex 34.000000 72.000000 -10.500000
      vertex 33.989040 72.209061 -10.500000
      vertex 34.000000 72.000000 23.000000
    endloop
  endfacet
  facet normal 0.994137 -0.108129 0.000000
    outer loop
      vertex 31.218704 -0.828024 -9.500000
      vertex 31.199999 -1.000000 -9.500000
      vertex 31.199999 -1.000000 -10.500000
    endloop
  endfacet
  facet normal 0.994137 -0.108129 0.000000
    outer loop
      vertex 31.218704 -0.828024 -9.500000
      vertex 31.199999 -1.000000 -10.500000
      vertex 31.218704 -0.828024 -10.500000
    endloop
  endfacet
  facet normal 0.947655 -0.319295 0.000000
    outer loop
      vertex 31.273939 -0.664089 -9.500000
      vertex 31.218704 -0.828024 -9.500000
      vertex 31.218704 -0.828024 -10.500000
    endloop
  endfacet
  facet normal 0.947655 -0.319295 0.000000
    outer loop
      vertex 31.273939 -0.664089 -9.500000
      vertex 31.218704 -0.828024 -10.500000
      vertex 31.273939 -0.664089 -10.500000
    endloop
  endfacet
  facet normal 0.856853 -0.515561 0.000000
    outer loop
      vertex 31.363127 -0.515861 -9.500000
      vertex 31.273939 -0.664089 -9.500000
      vertex 31.273939 -0.664089 -10.500000
    endloop
  endfacet
  facet normal 0.856853 -0.515561 0.000000
    outer loop
      vertex 31.363127 -0.515861 -9.500000
      vertex 31.273939 -0.664089 -10.500000
      vertex 31.363127 -0.515861 -10.500000
    endloop
  endfacet
  facet normal 0.726002 -0.687693 0.000000
    outer loop
      vertex 31.482090 -0.390270 -9.500000
      vertex 31.363127 -0.515861 -9.500000
      vertex 31.363127 -0.515861 -10.500000
    endloop
  endfacet
  facet normal 0.726002 -0.687693 0.000000
    outer loop
      vertex 31.482090 -0.390270 -9.500000
      vertex 31.363127 -0.515861 -10.500000
      vertex 31.482090 -0.390270 -10.500000
    endloop
  endfacet
  facet normal 0.561181 -0.827693 0.000000
    outer loop
      vertex 31.625275 -0.293190 -9.500000
      vertex 31.482090 -0.390270 -9.500000
      vertex 31.482090 -0.390270 -10.500000
    endloop
  endfacet
  facet normal 0.561181 -0.827693 0.000000
    outer loop
      vertex 31.625275 -0.293190 -9.500000
      vertex 31.482090 -0.390270 -10.500000
      vertex 31.625275 -0.293190 -10.500000
    endloop
  endfacet
  facet normal 0.370143 -0.928975 0.000000
    outer loop
      vertex 31.785976 -0.229160 -9.500000
      vertex 31.625275 -0.293190 -9.500000
      vertex 31.625275 -0.293190 -10.500000
    endloop
  endfacet
  facet normal 0.370143 -0.928975 0.000000
    outer loop
      vertex 31.785976 -0.229160 -9.500000
      vertex 31.625275 -0.293190 -10.500000
      vertex 31.785976 -0.229160 -10.500000
    endloop
  endfacet
  facet normal 0.161782 -0.986827 0.000000
    outer loop
      vertex 31.956688 -0.201173 -9.500000
      vertex 31.785976 -0.229160 -9.500000
      vertex 31.785976 -0.229160 -10.500000
    endloop
  endfacet
  facet normal 0.161782 -0.986827 0.000000
    outer loop
      vertex 31.956688 -0.201173 -9.500000
      vertex 31.785976 -0.229160 -10.500000
      vertex 31.956688 -0.201173 -10.500000
    endloop
  endfacet
  facet normal -0.054139 -0.998533 0.000000
    outer loop
      vertex 32.129425 -0.210539 -9.500000
      vertex 31.956688 -0.201173 -9.500000
      vertex 31.956688 -0.201173 -10.500000
    endloop
  endfacet
  facet normal -0.054139 -0.998533 -0.000000
    outer loop
      vertex 32.129425 -0.210539 -9.500000
      vertex 31.956688 -0.201173 -10.500000
      vertex 32.129425 -0.210539 -10.500000
    endloop
  endfacet
  facet normal -0.267531 -0.963549 0.000000
    outer loop
      vertex 32.296108 -0.256819 -9.500000
      vertex 32.129425 -0.210539 -9.500000
      vertex 32.129425 -0.210539 -10.500000
    endloop
  endfacet
  facet normal -0.267531 -0.963549 -0.000000
    outer loop
      vertex 32.296108 -0.256819 -9.500000
      vertex 32.129425 -0.210539 -10.500000
      vertex 32.296108 -0.256819 -10.500000
    endloop
  endfacet
  facet normal -0.468398 -0.883518 0.000000
    outer loop
      vertex 32.448952 -0.337849 -9.500000
      vertex 32.296108 -0.256819 -9.500000
      vertex 32.296108 -0.256819 -10.500000
    endloop
  endfacet
  facet normal -0.468398 -0.883518 -0.000000
    outer loop
      vertex 32.448952 -0.337849 -9.500000
      vertex 32.296108 -0.256819 -10.500000
      vertex 32.448952 -0.337849 -10.500000
    endloop
  endfacet
  facet normal -0.605180 -0.796088 0.000000
    outer loop
      vertex 32.517910 -0.390270 -9.500000
      vertex 32.448952 -0.337849 -9.500000
      vertex 32.448952 -0.337849 -10.500000
    endloop
  endfacet
  facet normal -0.605180 -0.796088 -0.000000
    outer loop
      vertex 32.517910 -0.390270 -9.500000
      vertex 32.448952 -0.337849 -10.500000
      vertex 32.517910 -0.390270 -10.500000
    endloop
  endfacet
  facet normal -0.725996 -0.687699 0.000000
    outer loop
      vertex 32.636875 -0.515861 -9.500000
      vertex 32.517910 -0.390270 -9.500000
      vertex 32.517910 -0.390270 -10.500000
    endloop
  endfacet
  facet normal -0.725996 -0.687699 -0.000000
    outer loop
      vertex 32.636875 -0.515861 -9.500000
      vertex 32.517910 -0.390270 -10.500000
      vertex 32.636875 -0.515861 -10.500000
    endloop
  endfacet
  facet normal -0.856863 -0.515545 0.000000
    outer loop
      vertex 32.726059 -0.664089 -9.500000
      vertex 32.636875 -0.515861 -9.500000
      vertex 32.636875 -0.515861 -10.500000
    endloop
  endfacet
  facet normal -0.856863 -0.515545 -0.000000
    outer loop
      vertex 32.726059 -0.664089 -9.500000
      vertex 32.636875 -0.515861 -10.500000
      vertex 32.726059 -0.664089 -10.500000
    endloop
  endfacet
  facet normal -0.947652 -0.319305 0.000000
    outer loop
      vertex 32.781296 -0.828024 -9.500000
      vertex 32.726059 -0.664089 -9.500000
      vertex 32.726059 -0.664089 -10.500000
    endloop
  endfacet
  facet normal -0.947652 -0.319305 -0.000000
    outer loop
      vertex 32.781296 -0.828024 -9.500000
      vertex 32.726059 -0.664089 -10.500000
      vertex 32.781296 -0.828024 -10.500000
    endloop
  endfacet
  facet normal -0.994138 -0.108118 0.000000
    outer loop
      vertex 32.799999 -1.000000 -9.500000
      vertex 32.781296 -0.828024 -9.500000
      vertex 32.781296 -0.828024 -10.500000
    endloop
  endfacet
  facet normal -0.994138 -0.108118 -0.000000
    outer loop
      vertex 32.799999 -1.000000 -9.500000
      vertex 32.781296 -0.828024 -10.500000
      vertex 32.799999 -1.000000 -10.500000
    endloop
  endfacet
  facet normal -0.994138 0.108118 0.000000
    outer loop
      vertex 32.781296 -1.171976 -9.500000
      vertex 32.799999 -1.000000 -9.500000
      vertex 32.799999 -1.000000 -10.500000
    endloop
  endfacet
  facet normal -0.994138 0.108118 0.000000
    outer loop
      vertex 32.781296 -1.171976 -9.500000
      vertex 32.799999 -1.000000 -10.500000
      vertex 32.781296 -1.171976 -10.500000
    endloop
  endfacet
  facet normal -0.947652 0.319305 0.000000
    outer loop
      vertex 32.726059 -1.335911 -9.500000
      vertex 32.781296 -1.171976 -9.500000
      vertex 32.781296 -1.171976 -10.500000
    endloop
  endfacet
  facet normal -0.947652 0.319305 0.000000
    outer loop
      vertex 32.726059 -1.335911 -9.500000
      vertex 32.781296 -1.171976 -10.500000
      vertex 32.726059 -1.335911 -10.500000
    endloop
  endfacet
  facet normal -0.856862 0.515545 0.000000
    outer loop
      vertex 32.636875 -1.484139 -9.500000
      vertex 32.726059 -1.335911 -9.500000
      vertex 32.726059 -1.335911 -10.500000
    endloop
  endfacet
  facet normal -0.856862 0.515545 0.000000
    outer loop
      vertex 32.636875 -1.484139 -9.500000
      vertex 32.726059 -1.335911 -10.500000
      vertex 32.636875 -1.484139 -10.500000
    endloop
  endfacet
  facet normal -0.725996 0.687698 0.000000
    outer loop
      vertex 32.517910 -1.609730 -9.500000
      vertex 32.636875 -1.484139 -9.500000
      vertex 32.636875 -1.484139 -10.500000
    endloop
  endfacet
  facet normal -0.725996 0.687698 0.000000
    outer loop
      vertex 32.517910 -1.609730 -9.500000
      vertex 32.636875 -1.484139 -10.500000
      vertex 32.517910 -1.609730 -10.500000
    endloop
  endfacet
  facet normal -0.605180 0.796088 0.000000
    outer loop
      vertex 32.448952 -1.662151 -9.500000
      vertex 32.517910 -1.609730 -9.500000
      vertex 32.517910 -1.609730 -10.500000
    endloop
  endfacet
  facet normal -0.605180 0.796088 0.000000
    outer loop
      vertex 32.448952 -1.662151 -9.500000
      vertex 32.517910 -1.609730 -10.500000
      vertex 32.448952 -1.662151 -10.500000
    endloop
  endfacet
  facet normal -0.515555 0.856856 0.000000
    outer loop
      vertex 32.374729 -1.706810 -9.500000
      vertex 32.448952 -1.662151 -9.500000
      vertex 32.448952 -1.662151 -10.500000
    endloop
  endfacet
  facet normal -0.515555 0.856856 0.000000
    outer loop
      vertex 32.374729 -1.706810 -9.500000
      vertex 32.448952 -1.662151 -10.500000
      vertex 32.374729 -1.706810 -10.500000
    endloop
  endfacet
  facet normal -0.370135 0.928978 0.000000
    outer loop
      vertex 32.214024 -1.770840 -9.500000
      vertex 32.374729 -1.706810 -9.500000
      vertex 32.374729 -1.706810 -10.500000
    endloop
  endfacet
  facet normal -0.370135 0.928978 0.000000
    outer loop
      vertex 32.214024 -1.770840 -9.500000
      vertex 32.374729 -1.706810 -10.500000
      vertex 32.214024 -1.770840 -10.500000
    endloop
  endfacet
  facet normal -0.161782 0.986827 0.000000
    outer loop
      vertex 32.043312 -1.798827 -9.500000
      vertex 32.214024 -1.770840 -9.500000
      vertex 32.214024 -1.770840 -10.500000
    endloop
  endfacet
  facet normal -0.161782 0.986827 0.000000
    outer loop
      vertex 32.043312 -1.798827 -9.500000
      vertex 32.214024 -1.770840 -10.500000
      vertex 32.043312 -1.798827 -10.500000
    endloop
  endfacet
  facet normal 0.054138 0.998533 0.000000
    outer loop
      vertex 31.870573 -1.789461 -9.500000
      vertex 32.043312 -1.798827 -9.500000
      vertex 32.043312 -1.798827 -10.500000
    endloop
  endfacet
  facet normal 0.054138 0.998533 0.000000
    outer loop
      vertex 31.870573 -1.789461 -9.500000
      vertex 32.043312 -1.798827 -10.500000
      vertex 31.870573 -1.789461 -10.500000
    endloop
  endfacet
  facet normal 0.267531 0.963549 0.000000
    outer loop
      vertex 31.703890 -1.743181 -9.500000
      vertex 31.870573 -1.789461 -9.500000
      vertex 31.870573 -1.789461 -10.500000
    endloop
  endfacet
  facet normal 0.267531 0.963549 0.000000
    outer loop
      vertex 31.703890 -1.743181 -9.500000
      vertex 31.870573 -1.789461 -10.500000
      vertex 31.703890 -1.743181 -10.500000
    endloop
  endfacet
  facet normal 0.468412 0.883510 0.000000
    outer loop
      vertex 31.551052 -1.662151 -9.500000
      vertex 31.703890 -1.743181 -9.500000
      vertex 31.703890 -1.743181 -10.500000
    endloop
  endfacet
  facet normal 0.468412 0.883510 0.000000
    outer loop
      vertex 31.551052 -1.662151 -9.500000
      vertex 31.703890 -1.743181 -10.500000
      vertex 31.551052 -1.662151 -10.500000
    endloop
  endfacet
  facet normal 0.647379 0.762168 0.000000
    outer loop
      vertex 31.419203 -1.550160 -9.500000
      vertex 31.551052 -1.662151 -9.500000
      vertex 31.551052 -1.662151 -10.500000
    endloop
  endfacet
  facet normal 0.647379 0.762168 0.000000
    outer loop
      vertex 31.419203 -1.550160 -9.500000
      vertex 31.551052 -1.662151 -10.500000
      vertex 31.419203 -1.550160 -10.500000
    endloop
  endfacet
  facet normal 0.796095 0.605172 0.000000
    outer loop
      vertex 31.314514 -1.412443 -9.500000
      vertex 31.419203 -1.550160 -9.500000
      vertex 31.419203 -1.550160 -10.500000
    endloop
  endfacet
  facet normal 0.796095 0.605172 0.000000
    outer loop
      vertex 31.314514 -1.412443 -9.500000
      vertex 31.419203 -1.550160 -10.500000
      vertex 31.314514 -1.412443 -10.500000
    endloop
  endfacet
  facet normal 0.907574 0.419892 0.000000
    outer loop
      vertex 31.241877 -1.255441 -9.500000
      vertex 31.314514 -1.412443 -9.500000
      vertex 31.314514 -1.412443 -10.500000
    endloop
  endfacet
  facet normal 0.907574 0.419892 0.000000
    outer loop
      vertex 31.241877 -1.255441 -9.500000
      vertex 31.314514 -1.412443 -10.500000
      vertex 31.241877 -1.255441 -10.500000
    endloop
  endfacet
  facet normal 0.976621 0.214969 0.000000
    outer loop
      vertex 31.204689 -1.086495 -9.500000
      vertex 31.241877 -1.255441 -9.500000
      vertex 31.241877 -1.255441 -10.500000
    endloop
  endfacet
  facet normal 0.976621 0.214969 0.000000
    outer loop
      vertex 31.204689 -1.086495 -9.500000
      vertex 31.241877 -1.255441 -10.500000
      vertex 31.204689 -1.086495 -10.500000
    endloop
  endfacet
  facet normal 0.998533 0.054145 0.000000
    outer loop
      vertex 31.199999 -1.000000 -9.500000
      vertex 31.204689 -1.086495 -9.500000
      vertex 31.204689 -1.086495 -10.500000
    endloop
  endfacet
  facet normal 0.998533 0.054145 0.000000
    outer loop
      vertex 31.199999 -1.000000 -9.500000
      vertex 31.204689 -1.086495 -10.500000
      vertex 31.199999 -1.000000 -10.500000
    endloop
  endfacet
  facet normal -0.052336 -0.998630 0.000000
    outer loop
      vertex -1.209057 -2.989044 23.000000
      vertex -1.000000 -3.000000 -10.500000
      vertex -1.000000 -3.000000 23.000000
    endloop
  endfacet
  facet normal -0.052336 -0.998630 0.000000
    outer loop
      vertex -1.209057 -2.989044 -10.500000
      vertex -1.000000 -3.000000 -10.500000
      vertex -1.209057 -2.989044 23.000000
    endloop
  endfacet
  facet normal -0.156434 -0.987688 0.000000
    outer loop
      vertex -1.209057 -2.989044 -10.500000
      vertex -1.209057 -2.989044 23.000000
      vertex -1.415823 -2.956295 23.000000
    endloop
  endfacet
  facet normal -0.156434 -0.987688 0.000000
    outer loop
      vertex -1.415823 -2.956295 -10.500000
      vertex -1.209057 -2.989044 -10.500000
      vertex -1.415823 -2.956295 23.000000
    endloop
  endfacet
  facet normal -0.258818 -0.965926 0.000000
    outer loop
      vertex -1.415823 -2.956295 -10.500000
      vertex -1.415823 -2.956295 23.000000
      vertex -1.618034 -2.902113 23.000000
    endloop
  endfacet
  facet normal -0.258818 -0.965926 0.000000
    outer loop
      vertex -1.618034 -2.902113 -10.500000
      vertex -1.415823 -2.956295 -10.500000
      vertex -1.618034 -2.902113 23.000000
    endloop
  endfacet
  facet normal -0.358368 -0.933580 0.000000
    outer loop
      vertex -1.618034 -2.902113 -10.500000
      vertex -1.618034 -2.902113 23.000000
      vertex -1.813473 -2.827091 23.000000
    endloop
  endfacet
  facet normal -0.358368 -0.933580 0.000000
    outer loop
      vertex -1.813473 -2.827091 -10.500000
      vertex -1.618034 -2.902113 -10.500000
      vertex -1.813473 -2.827091 23.000000
    endloop
  endfacet
  facet normal -0.453990 -0.891006 0.000000
    outer loop
      vertex -1.813473 -2.827091 -10.500000
      vertex -1.813473 -2.827091 23.000000
      vertex -2.000000 -2.732051 23.000000
    endloop
  endfacet
  facet normal -0.453990 -0.891006 0.000000
    outer loop
      vertex -2.000000 -2.732051 -10.500000
      vertex -1.813473 -2.827091 -10.500000
      vertex -2.000000 -2.732051 23.000000
    endloop
  endfacet
  facet normal -0.544640 -0.838670 0.000000
    outer loop
      vertex -2.000000 -2.732051 -10.500000
      vertex -2.000000 -2.732051 23.000000
      vertex -2.175570 -2.618034 23.000000
    endloop
  endfacet
  facet normal -0.544640 -0.838670 0.000000
    outer loop
      vertex -2.175570 -2.618034 -10.500000
      vertex -2.000000 -2.732051 -10.500000
      vertex -2.175570 -2.618034 23.000000
    endloop
  endfacet
  facet normal -0.629320 -0.777146 0.000000
    outer loop
      vertex -2.175570 -2.618034 -10.500000
      vertex -2.175570 -2.618034 23.000000
      vertex -2.338261 -2.486290 23.000000
    endloop
  endfacet
  facet normal -0.629320 -0.777146 0.000000
    outer loop
      vertex -2.338261 -2.486290 -10.500000
      vertex -2.175570 -2.618034 -10.500000
      vertex -2.338261 -2.486290 23.000000
    endloop
  endfacet
  facet normal -0.707107 -0.707107 0.000000
    outer loop
      vertex -2.338261 -2.486290 -10.500000
      vertex -2.338261 -2.486290 23.000000
      vertex -2.486290 -2.338261 23.000000
    endloop
  endfacet
  facet normal -0.707107 -0.707107 0.000000
    outer loop
      vertex -2.486290 -2.338261 -10.500000
      vertex -2.338261 -2.486290 -10.500000
      vertex -2.486290 -2.338261 23.000000
    endloop
  endfacet
  facet normal -0.777146 -0.629320 0.000000
    outer loop
      vertex -2.486290 -2.338261 -10.500000
      vertex -2.486290 -2.338261 23.000000
      vertex -2.618034 -2.175570 23.000000
    endloop
  endfacet
  facet normal -0.777146 -0.629320 0.000000
    outer loop
      vertex -2.618034 -2.175570 -10.500000
      vertex -2.486290 -2.338261 -10.500000
      vertex -2.618034 -2.175570 23.000000
    endloop
  endfacet
  facet normal -0.838670 -0.544640 0.000000
    outer loop
      vertex -2.618034 -2.175570 -10.500000
      vertex -2.618034 -2.175570 23.000000
      vertex -2.732051 -2.000000 23.000000
    endloop
  endfacet
  facet normal -0.838670 -0.544640 0.000000
    outer loop
      vertex -2.732051 -2.000000 -10.500000
      vertex -2.618034 -2.175570 -10.500000
      vertex -2.732051 -2.000000 23.000000
    endloop
  endfacet
  facet normal -0.891006 -0.453990 0.000000
    outer loop
      vertex -2.732051 -2.000000 -10.500000
      vertex -2.732051 -2.000000 23.000000
      vertex -2.827091 -1.813473 23.000000
    endloop
  endfacet
  facet normal -0.891006 -0.453990 0.000000
    outer loop
      vertex -2.827091 -1.813473 -10.500000
      vertex -2.732051 -2.000000 -10.500000
      vertex -2.827091 -1.813473 23.000000
    endloop
  endfacet
  facet normal -0.933580 -0.358368 0.000000
    outer loop
      vertex -2.827091 -1.813473 -10.500000
      vertex -2.827091 -1.813473 23.000000
      vertex -2.902113 -1.618034 23.000000
    endloop
  endfacet
  facet normal -0.933580 -0.358368 0.000000
    outer loop
      vertex -2.902113 -1.618034 -10.500000
      vertex -2.827091 -1.813473 -10.500000
      vertex -2.902113 -1.618034 23.000000
    endloop
  endfacet
  facet normal -0.965926 -0.258818 0.000000
    outer loop
      vertex -2.902113 -1.618034 -10.500000
      vertex -2.902113 -1.618034 23.000000
      vertex -2.956295 -1.415823 23.000000
    endloop
  endfacet
  facet normal -0.965926 -0.258818 0.000000
    outer loop
      vertex -2.956295 -1.415823 -10.500000
      vertex -2.902113 -1.618034 -10.500000
      vertex -2.956295 -1.415823 23.000000
    endloop
  endfacet
  facet normal -0.987688 -0.156434 0.000000
    outer loop
      vertex -2.956295 -1.415823 -10.500000
      vertex -2.956295 -1.415823 23.000000
      vertex -2.989044 -1.209057 23.000000
    endloop
  endfacet
  facet normal -0.987688 -0.156434 0.000000
    outer loop
      vertex -2.989044 -1.209057 -10.500000
      vertex -2.956295 -1.415823 -10.500000
      vertex -2.989044 -1.209057 23.000000
    endloop
  endfacet
  facet normal -0.998630 -0.052336 0.000000
    outer loop
      vertex -2.989044 -1.209057 -10.500000
      vertex -2.989044 -1.209057 23.000000
      vertex -3.000000 -1.000000 23.000000
    endloop
  endfacet
  facet normal -0.998630 -0.052336 0.000000
    outer loop
      vertex -3.000000 -1.000000 -10.500000
      vertex -2.989044 -1.209057 -10.500000
      vertex -3.000000 -1.000000 23.000000
    endloop
  endfacet
  facet normal 0.052336 -0.998630 0.000000
    outer loop
      vertex 32.209057 -2.989044 -10.500000
      vertex 32.000000 -3.000000 23.000000
      vertex 32.000000 -3.000000 -10.500000
    endloop
  endfacet
  facet normal 0.052336 -0.998630 0.000000
    outer loop
      vertex 32.209057 -2.989044 23.000000
      vertex 32.000000 -3.000000 23.000000
      vertex 32.209057 -2.989044 -10.500000
    endloop
  endfacet
  facet normal 0.156436 -0.987688 0.000000
    outer loop
      vertex 32.209057 -2.989044 23.000000
      vertex 32.209057 -2.989044 -10.500000
      vertex 32.415821 -2.956295 -10.500000
    endloop
  endfacet
  facet normal 0.156436 -0.987688 0.000000
    outer loop
      vertex 32.415821 -2.956295 23.000000
      vertex 32.209057 -2.989044 23.000000
      vertex 32.415821 -2.956295 -10.500000
    endloop
  endfacet
  facet normal 0.258815 -0.965927 0.000000
    outer loop
      vertex 32.415821 -2.956295 23.000000
      vertex 32.415821 -2.956295 -10.500000
      vertex 32.618034 -2.902113 -10.500000
    endloop
  endfacet
  facet normal 0.258815 -0.965927 0.000000
    outer loop
      vertex 32.618034 -2.902113 23.000000
      vertex 32.415821 -2.956295 23.000000
      vertex 32.618034 -2.902113 -10.500000
    endloop
  endfacet
  facet normal 0.358370 -0.933580 0.000000
    outer loop
      vertex 32.618034 -2.902113 23.000000
      vertex 32.618034 -2.902113 -10.500000
      vertex 32.813473 -2.827091 -10.500000
    endloop
  endfacet
  facet normal 0.358370 -0.933580 0.000000
    outer loop
      vertex 32.813473 -2.827091 23.000000
      vertex 32.618034 -2.902113 23.000000
      vertex 32.813473 -2.827091 -10.500000
    endloop
  endfacet
  facet normal 0.453989 -0.891007 0.000000
    outer loop
      vertex 32.813473 -2.827091 23.000000
      vertex 32.813473 -2.827091 -10.500000
      vertex 33.000000 -2.732051 -10.500000
    endloop
  endfacet
  facet normal 0.453989 -0.891007 0.000000
    outer loop
      vertex 33.000000 -2.732051 23.000000
      vertex 32.813473 -2.827091 23.000000
      vertex 33.000000 -2.732051 -10.500000
    endloop
  endfacet
  facet normal 0.544646 -0.838666 0.000000
    outer loop
      vertex 33.000000 -2.732051 23.000000
      vertex 33.000000 -2.732051 -10.500000
      vertex 33.175568 -2.618034 -10.500000
    endloop
  endfacet
  facet normal 0.544646 -0.838666 0.000000
    outer loop
      vertex 33.175568 -2.618034 23.000000
      vertex 33.000000 -2.732051 23.000000
      vertex 33.175568 -2.618034 -10.500000
    endloop
  endfacet
  facet normal 0.629314 -0.777151 0.000000
    outer loop
      vertex 33.175568 -2.618034 23.000000
      vertex 33.175568 -2.618034 -10.500000
      vertex 33.338261 -2.486290 -10.500000
    endloop
  endfacet
  facet normal 0.629314 -0.777151 0.000000
    outer loop
      vertex 33.338261 -2.486290 23.000000
      vertex 33.175568 -2.618034 23.000000
      vertex 33.338261 -2.486290 -10.500000
    endloop
  endfacet
  facet normal 0.707114 -0.707099 0.000000
    outer loop
      vertex 33.338261 -2.486290 23.000000
      vertex 33.338261 -2.486290 -10.500000
      vertex 33.486286 -2.338261 -10.500000
    endloop
  endfacet
  facet normal 0.707114 -0.707099 0.000000
    outer loop
      vertex 33.486286 -2.338261 23.000000
      vertex 33.338261 -2.486290 23.000000
      vertex 33.486286 -2.338261 -10.500000
    endloop
  endfacet
  facet normal 0.777137 -0.629332 0.000000
    outer loop
      vertex 33.486286 -2.338261 23.000000
      vertex 33.486286 -2.338261 -10.500000
      vertex 33.618034 -2.175570 -10.500000
    endloop
  endfacet
  facet normal 0.777137 -0.629332 0.000000
    outer loop
      vertex 33.618034 -2.175570 23.000000
      vertex 33.486286 -2.338261 23.000000
      vertex 33.618034 -2.175570 -10.500000
    endloop
  endfacet
  facet normal 0.838677 -0.544629 0.000000
    outer loop
      vertex 33.618034 -2.175570 23.000000
      vertex 33.618034 -2.175570 -10.500000
      vertex 33.732048 -2.000000 -10.500000
    endloop
  endfacet
  facet normal 0.838677 -0.544629 0.000000
    outer loop
      vertex 33.732048 -2.000000 23.000000
      vertex 33.618034 -2.175570 23.000000
      vertex 33.732048 -2.000000 -10.500000
    endloop
  endfacet
  facet normal 0.891001 -0.454002 0.000000
    outer loop
      vertex 33.732048 -2.000000 23.000000
      vertex 33.732048 -2.000000 -10.500000
      vertex 33.827091 -1.813473 -10.500000
    endloop
  endfacet
  facet normal 0.891001 -0.454002 0.000000
    outer loop
      vertex 33.827091 -1.813473 23.000000
      vertex 33.732048 -2.000000 23.000000
      vertex 33.827091 -1.813473 -10.500000
    endloop
  endfacet
  facet normal 0.933584 -0.358358 0.000000
    outer loop
      vertex 33.827091 -1.813473 23.000000
      vertex 33.827091 -1.813473 -10.500000
      vertex 33.902111 -1.618034 -10.500000
    endloop
  endfacet
  facet normal 0.933584 -0.358358 0.000000
    outer loop
      vertex 33.902111 -1.618034 23.000000
      vertex 33.827091 -1.813473 23.000000
      vertex 33.902111 -1.618034 -10.500000
    endloop
  endfacet
  facet normal 0.965924 -0.258827 0.000000
    outer loop
      vertex 33.902111 -1.618034 23.000000
      vertex 33.902111 -1.618034 -10.500000
      vertex 33.956295 -1.415823 -10.500000
    endloop
  endfacet
  facet normal 0.965924 -0.258827 0.000000
    outer loop
      vertex 33.956295 -1.415823 23.000000
      vertex 33.902111 -1.618034 23.000000
      vertex 33.956295 -1.415823 -10.500000
    endloop
  endfacet
  facet normal 0.987691 -0.156419 0.000000
    outer loop
      vertex 33.956295 -1.415823 23.000000
      vertex 33.956295 -1.415823 -10.500000
      vertex 33.989040 -1.209057 -10.500000
    endloop
  endfacet
  facet normal 0.987691 -0.156419 0.000000
    outer loop
      vertex 33.989040 -1.209057 23.000000
      vertex 33.956295 -1.415823 23.000000
      vertex 33.989040 -1.209057 -10.500000
    endloop
  endfacet
  facet normal 0.998629 -0.052352 0.000000
    outer loop
      vertex 33.989040 -1.209057 23.000000
      vertex 33.989040 -1.209057 -10.500000
      vertex 34.000000 -1.000000 -10.500000
    endloop
  endfacet
  facet normal 0.998629 -0.052352 0.000000
    outer loop
      vertex 34.000000 -1.000000 23.000000
      vertex 33.989040 -1.209057 23.000000
      vertex 34.000000 -1.000000 -10.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 22.000000 -1.500000 15.500000
      vertex 22.000000 0.000000 15.500000
      vertex 18.400000 0.000000 15.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 22.000000 -1.500000 15.500000
      vertex 18.400000 0.000000 15.500000
      vertex 18.400000 -1.000000 15.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 22.000000 -1.500000 15.500000
      vertex 18.400000 -1.000000 15.500000
      vertex 18.410957 -1.209057 15.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 22.000000 -1.500000 15.500000
      vertex 18.410957 -1.209057 15.500000
      vertex 18.443705 -1.415823 15.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 18.463509 -1.500000 15.500000
      vertex 22.000000 -1.500000 15.500000
      vertex 18.443705 -1.415823 15.500000
    endloop
  endfacet
  facet normal -1.000000 0.000000 -0.000000
    outer loop
      vertex 22.000000 0.000000 23.000000
      vertex 22.000000 0.000000 15.500000
      vertex 22.000000 -1.500000 15.500000
    endloop
  endfacet
  facet normal -1.000000 -0.000000 0.000000
    outer loop
      vertex 22.000000 0.000000 23.000000
      vertex 22.000000 -1.500000 15.500000
      vertex 22.000000 -1.500000 23.000000
    endloop
  endfacet
  facet normal 1.000000 0.000000 0.000000
    outer loop
      vertex 7.000000 -1.500000 23.000000
      vertex 7.000000 -1.500000 15.500000
      vertex 7.000000 0.000000 15.500000
    endloop
  endfacet
  facet normal 1.000000 -0.000000 0.000000
    outer loop
      vertex 7.000000 -1.500000 23.000000
      vertex 7.000000 0.000000 15.500000
      vertex 7.000000 0.000000 23.000000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 9.836493 -1.500000 15.763508
      vertex 9.836493 -1.500000 15.500000
      vertex 7.000000 -1.500000 15.500000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 9.836493 -1.500000 15.763508
      vertex 7.000000 -1.500000 15.500000
      vertex 7.000000 -1.500000 23.000000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 18.463509 -1.500000 15.763508
      vertex 9.836493 -1.500000 15.763508
      vertex 7.000000 -1.500000 23.000000
    endloop
  endfacet
  facet normal 0.000000 1.000000 -0.000000
    outer loop
      vertex 18.463509 -1.500000 15.763508
      vertex 7.000000 -1.500000 23.000000
      vertex 22.000000 -1.500000 23.000000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 18.463509 -1.500000 15.500000
      vertex 18.463509 -1.500000 15.763508
      vertex 22.000000 -1.500000 23.000000
    endloop
  endfacet
  facet normal 0.000000 1.000000 0.000000
    outer loop
      vertex 18.463509 -1.500000 15.500000
      vertex 22.000000 -1.500000 23.000000
      vertex 22.000000 -1.500000 15.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 9.856295 -1.415823 15.500000
      vertex 7.000000 -1.500000 15.500000
      vertex 9.836493 -1.500000 15.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 9.900000 -1.000000 15.500000
      vertex 9.900000 0.000000 15.500000
      vertex 7.000000 0.000000 15.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 9.900000 -1.000000 15.500000
      vertex 7.000000 0.000000 15.500000
      vertex 7.000000 -1.500000 15.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 9.889044 -1.209057 15.500000
      vertex 9.900000 -1.000000 15.500000
      vertex 7.000000 -1.500000 15.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 9.889044 -1.209057 15.500000
      vertex 7.000000 -1.500000 15.500000
      vertex 9.856295 -1.415823 15.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 3.000000 3.000000 -4.500000
      vertex 4.565767 1.952703 -4.500000
      vertex 4.673516 2.034611 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 7.750000 -1.000000 -4.500000
      vertex 6.595776 0.731287 -4.500000
      vertex 6.559566 0.600873 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 7.750000 3.000000 -4.500000
      vertex 6.595776 1.268713 -4.500000
      vertex 6.617672 1.135149 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 7.750000 3.000000 -4.500000
      vertex 6.617672 1.135149 -4.500000
      vertex 6.625000 1.000000 -4.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 7.750000 -1.000000 -4.500000
      vertex 7.750000 3.000000 -4.500000
      vertex 6.625000 1.000000 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 7.750000 -1.000000 -4.500000
      vertex 6.625000 1.000000 -4.500000
      vertex 6.617672 0.864851 -4.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 6.595776 0.731287 -4.500000
      vertex 7.750000 -1.000000 -4.500000
      vertex 6.617672 0.864851 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 7.750000 -1.000000 -4.500000
      vertex 6.559566 0.600873 -4.500000
      vertex 6.509470 0.475139 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 7.750000 -1.000000 -4.500000
      vertex 6.509470 0.475139 -4.500000
      vertex 6.446072 0.355558 -4.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 6.370117 0.243532 -4.500000
      vertex 7.750000 -1.000000 -4.500000
      vertex 6.446072 0.355558 -4.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 4.467505 1.859624 -4.500000
      vertex 4.565767 1.952703 -4.500000
      vertex 3.000000 3.000000 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 3.000000 3.000000 -4.500000
      vertex 4.673516 2.034611 -4.500000
      vertex 4.789489 2.104390 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 3.000000 3.000000 -4.500000
      vertex 4.789489 2.104390 -4.500000
      vertex 4.912327 2.161221 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 5.040590 2.204437 -4.500000
      vertex 3.000000 3.000000 -4.500000
      vertex 4.912327 2.161221 -4.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 5.709411 2.204437 -4.500000
      vertex 5.837673 2.161221 -4.500000
      vertex 7.750000 3.000000 -4.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 5.709411 2.204437 -4.500000
      vertex 7.750000 3.000000 -4.500000
      vertex 5.577228 2.233533 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 7.750000 3.000000 -4.500000
      vertex 5.837673 2.161221 -4.500000
      vertex 5.960511 2.104390 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 7.750000 3.000000 -4.500000
      vertex 5.960511 2.104390 -4.500000
      vertex 6.076484 2.034611 -4.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 6.184233 1.952703 -4.500000
      vertex 7.750000 3.000000 -4.500000
      vertex 6.076484 2.034611 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 7.750000 3.000000 -4.500000
      vertex 6.184233 1.952703 -4.500000
      vertex 6.282495 1.859624 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 7.750000 3.000000 -4.500000
      vertex 6.282495 1.859624 -4.500000
      vertex 6.370117 1.756468 -4.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 6.446072 1.644442 -4.500000
      vertex 7.750000 3.000000 -4.500000
      vertex 6.370117 1.756468 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 7.750000 -1.000000 -4.500000
      vertex 6.370117 0.243532 -4.500000
      vertex 6.282495 0.140376 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 7.750000 -1.000000 -4.500000
      vertex 6.282495 0.140376 -4.500000
      vertex 6.184233 0.047297 -4.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 6.076484 -0.034611 -4.500000
      vertex 7.750000 -1.000000 -4.500000
      vertex 6.184233 0.047297 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 7.750000 -1.000000 -4.500000
      vertex 6.076484 -0.034611 -4.500000
      vertex 5.960511 -0.104390 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 7.750000 -1.000000 -4.500000
      vertex 5.960511 -0.104390 -4.500000
      vertex 5.837673 -0.161221 -4.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 5.709411 -0.204437 -4.500000
      vertex 7.750000 -1.000000 -4.500000
      vertex 5.837673 -0.161221 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 3.000000 0.000000 -4.500000
      vertex 4.154224 0.731287 -4.500000
      vertex 4.132328 0.864851 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 3.000000 3.000000 -4.500000
      vertex 5.040590 2.204437 -4.500000
      vertex 5.172772 2.233533 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 3.000000 3.000000 -4.500000
      vertex 5.172772 2.233533 -4.500000
      vertex 5.307327 2.248167 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 7.750000 3.000000 -4.500000
      vertex 3.000000 3.000000 -4.500000
      vertex 5.307327 2.248167 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 7.750000 3.000000 -4.500000
      vertex 5.307327 2.248167 -4.500000
      vertex 5.442674 2.248167 -4.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 5.577228 2.233533 -4.500000
      vertex 7.750000 3.000000 -4.500000
      vertex 5.442674 2.248167 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 7.750000 3.000000 -4.500000
      vertex 6.446072 1.644442 -4.500000
      vertex 6.509470 1.524861 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 7.750000 3.000000 -4.500000
      vertex 6.509470 1.524861 -4.500000
      vertex 6.559566 1.399127 -4.500000
    endloop
  endfacet
  facet normal 0.000000 -0.000000 1.000000
    outer loop
      vertex 6.595776 1.268713 -4.500000
      vertex 7.750000 3.000000 -4.500000
      vertex 6.559566 1.399127 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 3.000000 -1.000000 -4.500000
      vertex 4.789489 -0.104390 -4.500000
      vertex 4.673516 -0.034611 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 3.000000 -1.000000 -4.500000
      vertex 4.673516 -0.034611 -4.500000
      vertex 4.565767 0.047297 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 4.467505 0.140376 -4.500000
      vertex 3.000000 -1.000000 -4.500000
      vertex 4.565767 0.047297 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 4.190434 0.600873 -4.500000
      vertex 4.154224 0.731287 -4.500000
      vertex 3.000000 0.000000 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 3.000000 3.000000 -4.500000
      vertex 4.190434 1.399127 -4.500000
      vertex 4.240530 1.524861 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 3.000000 -1.000000 -4.500000
      vertex 4.467505 0.140376 -4.500000
      vertex 4.379884 0.243532 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 3.000000 -1.000000 -4.500000
      vertex 4.379884 0.243532 -4.500000
      vertex 4.303928 0.355558 -4.500000
    endloop
  endfacet
  facet normal -0.000000 0.000000 1.000000
    outer loop
      vertex 3.000000 0.000000 -4.500000
      vertex 3.000000 -1.000000 -4.500000
      vertex 4.303928 0.355558 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 3.000000 0.000000 -4.500000
      vertex 4.303928 0.355558 -4.500000
      vertex 4.240530 0.475139 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 4.190434 0.600873 -4.500000
      vertex 3.000000 0.000000 -4.500000
      vertex 4.240530 0.475139 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 3.000000 3.000000 -4.500000
      vertex 4.240530 1.524861 -4.500000
      vertex 4.303928 1.644442 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 3.000000 3.000000 -4.500000
      vertex 4.303928 1.644442 -4.500000
      vertex 4.379884 1.756468 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 4.467505 1.859624 -4.500000
      vertex 3.000000 3.000000 -4.500000
      vertex 4.379884 1.756468 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 7.750000 -1.000000 -4.500000
      vertex 5.709411 -0.204437 -4.500000
      vertex 5.577228 -0.233533 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 7.750000 -1.000000 -4.500000
      vertex 5.577228 -0.233533 -4.500000
      vertex 5.442674 -0.248167 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 3.000000 -1.000000 -4.500000
      vertex 7.750000 -1.000000 -4.500000
      vertex 5.442674 -0.248167 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 3.000000 -1.000000 -4.500000
      vertex 5.442674 -0.248167 -4.500000
      vertex 5.307327 -0.248167 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 5.172772 -0.233533 -4.500000
      vertex 3.000000 -1.000000 -4.500000
      vertex 5.307327 -0.248167 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 3.000000 -1.000000 -4.500000
      vertex 5.172772 -0.233533 -4.500000
      vertex 5.040590 -0.204437 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 3.000000 -1.000000 -4.500000
      vertex 5.040590 -0.204437 -4.500000
      vertex 4.912327 -0.161221 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 4.789489 -0.104390 -4.500000
      vertex 3.000000 -1.000000 -4.500000
      vertex 4.912327 -0.161221 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 3.000000 0.000000 -4.500000
      vertex 4.132328 0.864851 -4.500000
      vertex 4.125000 1.000000 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 3.000000 0.000000 -4.500000
      vertex 4.125000 1.000000 -4.500000
      vertex 4.132328 1.135149 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 3.000000 3.000000 -4.500000
      vertex 3.000000 0.000000 -4.500000
      vertex 4.132328 1.135149 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 3.000000 3.000000 -4.500000
      vertex 4.132328 1.135149 -4.500000
      vertex 4.154224 1.268713 -4.500000
    endloop
  endfacet
  facet normal 0.000000 0.000000 1.000000
    outer loop
      vertex 4.190434 1.399127 -4.500000
      vertex 3.000000 3.000000 -4.500000
      vertex 4.154224 1.268713 -4.500000
    endloop
  endfacet
endsolid Mesh

```


