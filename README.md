# Gmuli-Bazi-Calc

A web-based calculator for generating BaZi (Four Pillars of Destiny) charts using JavaScript.

We tried many different ways of doing this on the website. The big bazi calculator using PyEphem is using XEphem.The big astro calculator is using the  Python extension of AstroDienst’s Swiss Ephemeris library, while most of the old calculators are using orb v2 and js_astro, both using VSOP(https://github.com/astsakai/js_astro).

The idea is that not all calculators need high accuracy. For 8 mansions calculator, the position of the Sun that is calculated once a year, will be in play so rarily that it makes sense to have something faster instead, for example. Focus was on variaty instead, so for different uses one can check different libraries.

The idea for me, is that with all that tested, there is an optimal path showing up. That is much faster and less resource heavy, at the same time as accurate as it can get. Then fully open sourcing that seems the right thing to do, as usual. This won't be Creative Common, we will add it as MiT,so don't need to mention us here, can do whatever you want with it.

So what exactly it is... Well, with skyfield we have made a list of all points when in UTC time the Sun crosses a Solar Term longitude. So we have .txt files with that, may change them to .js later on for ease of use. It changes the month pillar based on the dates of the Solar Terms around the given date. The smaller one with dates 1900-2050 is loaded initially, then if date is provided outside that scope the big one is loaded too covering 0 to 2150.

All this calculates in UTC time, so if there is a few hour differences, check if your timezone is added to it.

The .txt times and dates are made with Skyfield using JPL ephemerides.

## Features
- Converts Gregorian date/time into Chinese Four Pillars
- Handles Heavenly Stems, Earthly Branches, and 60 Jiazi cycle
- Pure JS, works in-browser
- Switched dates depending on what is added
- Potentially very accurate for the small size

## Usage
Clone the repo and open `bazidates.html` in your browser.

## License
MIT 
