
# YouTube Exclusion List Builder

This project aim to help digital marketing professional to improve their Google Ads placements on YouTube campaign. 
It's always frustrating to see part of campaign budget going to videos with kid content, undesired topic like music or
wrong spoken language.
Unfortunately exclusion list available online are not the most reliable and up to date.

This graphic user interface will help you to build along your campaign custom YouTube channel exclusion list.


## Installation

**1<sup>st</sup> option - Install YouTube Exclusion List Builder with executable file.**

You can download the application here [YouTube-Exclusion-List-Builder.v1.0.zip
](https://github.com/seexmax/YouTube-Exclusion-List-Builder/releases/tag/v1.0.0) 
for macOS or Windows. 

On Mac, you will most probably face an error message while executing the file like 
" 'YouTube-Exclusion-List-Builder.v1.0' can’t be opened because Apple cannot check it for malicious software.". 
To avoid this, go in the System Preferences > Security and Privacy and you should see a section where it says 
that the app was blocked from use. Click on open anyway. Wait a minute and you should see the app open.


**2<sup>nd</sup> option - Install YouTube Exclusion List Builder with command line.**

This project requires python 3.10 you can download it [here](https://www.python.org/downloads/release/python-3100/).

```bash
git clone https://github.com/seexmax/YouTube-Exclusion-List-Builder.git
```
Open the project directory with `cd` and install the requirements. 
```bash
pip install -r requirements.txt
```
On Ubuntu and other Debian-based Linux distributions you will also need to install tkinter.
```bash
sudo apt install python3-tk
```
In the project directory run `main.py` file to execute the application.
```bash
python3 main.py
```

## Demo
**The application is made of two tabs.**  
* The first tab is where you will upload the Excel file with the YouTube channels you want to check.
Please note that you need to use the template available 
[here](/template_excel_file.xlsx) 
for formatting purposes. Only `.xlsx` format can be uploaded on the application.

<img height="50%" src="https://github.com/seexmax/YouTube-MadeForKid-Checker/assets/96994915/a41f0f31-cdec-4543-9aa9-8f59bb8db0e6" width="50%"/>

* On the second tab you need to enter your YouTube API token. If you don't know to get one you can click on `How to get a token ?`.
Instructions to get a token will be shown. Note that a token is limited to 10.000 requests per day. If you would like
to process more than 10.000 channels you will need to use multiple API token or wait the next day.

<img height="50%" src="https://github.com/seexmax/YouTube-MadeForKid-Checker/assets/96994915/ccb62a79-a602-4768-86ee-c854e1875447" width="50%"/>

Once you enter a valid token and upload an Excel file matching the template, the application will show you
how many channels are in your file. Note that the button `Process channels` is now clickable to start the process.

<img height="50%" src="https://github.com/seexmax/YouTube-MadeForKid-Checker/assets/96994915/595494ff-8921-4363-bddd-a652677f4259" width="50%"/>

As the application processes the channels, the time left will be displayed. At anytime during the process you can click 
on `Stop & Save`, it will interrupt the process and save the data collected in your file.

<img height="50%" src="https://github.com/seexmax/YouTube-MadeForKid-Checker/assets/96994915/f521aeda-de50-478d-ab76-fb8a68353148" width="50%"/>

When the application is done, or you used `Stop & Save`, the data collected will be saved in your file on a new tab named
`Results`.

<img height="50%" src="https://github.com/seexmax/YouTube-MadeForKid-Checker/assets/96994915/9acf09cf-28f4-4f55-8d8f-e2181de8e360" width="50%"/>

If you didn't process all the channels of your file because you reached the quota limitation of your token, or you used
`Stop & Save`, you can always upload again your file to process the remaining channels. The application will automatically
detect your `Results` tab and start from where you left.  
_You can see from the example of the demo that the channels to process went from 9.750 to 9.096 when I upload the file 
again._

<img height="50%" src="https://github.com/seexmax/YouTube-MadeForKid-Checker/assets/96994915/04bf958c-5773-4962-b917-6f65db9b7480" width="50%"/>

**The results in your Excel file.**  

When the process is complete your data will be saved in the `Results` tab. You will see four new columns, `madeForKids` which 
indicates if the channel is made for kids or not. `Description` which contains the description of the channel. `Default Language`
which is the main language used on the channel. `Topic` which describe the content type of the channel. You can now filter 
with any element you want and build your exclusion list.

<img height="50%" alt="Screenshot_7" src="https://github.com/seexmax/YouTube-MadeForKids-Checker/assets/96994915/8a662455-2fbb-4338-ba57-bed666be2ae4" width="50%"/>

The `Description` column is also useful when 'No data' appears in `madeForKids`. You can use the _Find & Replace_ Excel tool 
to search for keywords such as 'kids' or 'fairytale' and add the matching channels to your list.

## Upcoming updates

* Additional filtering options such as language. (Already available for the 2<sup>nd</sup> installation option)
* Moving the application to a more general exclusion list builder. (Done for the 2<sup>nd</sup> installation option)

## License

[MIT](https://choosealicense.com/licenses/mit/)

