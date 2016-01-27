# google_traffic

Google Maps tool for obtaining estimated trip times.

## Description

traffic_times.py is a Python 2 script that retrieves 3 travel duration estimates working off the assuption that you depart at the current time.

## Google API Key Requirements

For this project, you'll need a Google API Key. You can do so here:
https://developers.google.com/maps/documentation/javascript/get-api-key#key

1. Create a Google Developer Project. [Link](https://console.developers.google.com/project)
2. Enable Google Maps Directions API.
  1. Click 'Use Google APIs' (a blue box).
  2. Stay on Overview tab.
  3. Click more in Google Maps API section.
  4. Click 'Google Maps Directions API'.
  5. Click 'Enable API' button.
3. Create Server API Key.
  1. Click Credentials tab.
  2. Click New credentials.
  3. Click API key.
  4. Click Server key.
  5. Name your key.
  6. Click Create.
  7. Copy your key.
4. Set googleMaps.self.key to your API key.

## Usage

You can run it via "python traffic_times.py to_work" to output times from the "home" variable to the "work" variable in the script, or "python traffic_times.py from_work" for the reverse.

### Recommended Setup

I have my crontab setup to run the following:

Run to_work during morning commute times:
*/10 11-15 * * 1-5 /usr/bin/python traffic_times.py to_work
Run from_work during evening commute times:
*/10 19-23 * * 1-5 /usr/bin/python traffic_times.py from_work

I run the r script from time to time to update graphs (Rscript traffic_plots.R)

*******************************************************************************
MIT License
Copyright (c) 2016 Michael Smith

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

*******************************************************************************


