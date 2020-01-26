---
layout: post
title: "Renewable energy landscape in India"
comments: true
description: "A snapshot of installed capacity in India"
keywords: "India, Power Generation, Renewables"
---

A couple of weeks ago, I came across a headline in the newspaper that said, "India's renewable energy capacity crosses 80GW-mark: Govt tells Rajya Sabha" ([business-standard article](https://www.business-standard.com/article/pti-stories/india-s-renewable-energy-capacity-crosses-80gw-mark-says-r-k-singh-119071600668_1.html)). It certainly feels like an impressive achievement. In college, we discussed, studied, analyzed and simulated thermal power plants in the courses. Renewables at the time was a great idea for the future. When I say this, I am not talking about a time decades ago; this is an experience from 7-8 years ago. In the recent past, we have seen tremendous growth in renewables and a large effort being put towards bringing more and more renewables online.

I took this opportunity to study the power generation landscape in India. I was curious to see state wise distribution of installed capacity by source as well as state wise planned capacity. The Government of India through the open data initiative makes tremendous amounts of data available at fingertips. It took me a few hours of sifting through the data.gov.in website to find just the right kind of datasets.

The first challenge was to learn how to plot data on the maps. I explored a couple of python libraries which allow plotting data on the map, Basemap and Geopandas. Of the two, Geopandas is not only very easy to use, it offers a very intuitive interface to plot the data and modify as you'd like. You can compare the complexity of code between Basemap and Geopandas in the notebooks linked below.

Thermal power has been the number one source of electricity. ~ 64% of the total electricity comes from thermal power plants powered on some type of fuel such as coal, natural gas, diesel etc. Having signed the Paris Climate Accord, India has agreed to review and limit use of coal power plants. In comparison, Nuclear (~2%) and Hydro (~13%) represent smaller contribution. Increasingly larger contribution is made through renewables, which as of July 2019 stands ~22%.


![Installed Capacity](https://media-exp2.licdn.com/dms/image/C5612AQF8jrcWsEoVig/article-inline_image-shrink_1500_2232/0?e=1585785600&v=beta&t=K41vWyY7XxOqHQMX-UsVDg9xX7uGnh811AUHl-oaX3c)

The Government has set a target of installing 100 GW of solar capacity by 2022 in the country.  A target of installing 175 GW of renewable energy capacity by the year 2022 has been set, which includes 100 GW from solar, 60 GW from wind, 10 GW from bio-power and 5 GW from small hydro-power.

![Renewable Installed Capacity](https://media-exp2.licdn.com/dms/image/C5612AQGIo0Vh5StqIA/article-inline_image-shrink_1500_2232/0?e=1585785600&v=beta&t=UBfXwfCrXz2pQA0PnCXKVpZ-STHrM0ecrUpX44yCGsc)

Two primary factors influence India's heavy focus on Wind and Solar. 1) India has the lowest capital cost for solar project in the world. 2) The government has worked towards developing strong partnerships with international partners as well as building domestic suppliers to build the necessary capacity. Based on the latest Rajyasabha figures, India looks on the track towards meeting the 175GW goal by 2022!

For datasets, notebook and more comments: [GitHub](https://github.com/jaydeshpande/India-Power-Generation)
