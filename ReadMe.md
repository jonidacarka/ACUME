To Run:

1)Download project files from git

2)Place your excel files in the data folder, and in the test folder
  place your test files 

3)Update configs.py file to your needs

  files_path  

    update if you want to not use the data folder but some other folder you might want, for ease it should be inside the directory 


include_types 

    list with the data types (file extension) that you want to consider
    in the calculations. if you want to add a new one , add an element to list like
    include_types = ['a','b'] where a , b file types

exclude_strings 

    ignores all files with name containg the string.
    Useful if there are test files, or helper files in the data folder that you want to reject


sorting_orders 

    list of dictionaries. 

    4 dictionaries , each representing a different type of order
    The first dictionary - how the order for calculation of IFA will be
    
    The second dictionary - how the order for calculation of perfect order (denominator in PopX,Pop General)
    
    The third dictionary - how the order for calculation of nominator for optimal in pop general
    
    The fourth dictionary - how th order for calculation of nominator for worse in pop general


start_value, end_value , step

    configurable values for popX. Usually are 10,50,5
    but can be changeable to user needs

get_configs 

    how the file output will be named

normalize_json

    a dictionary of dictionaries
    change optimal and worst to need, careful about 
    the field of choice


To Run the code
    
    If python installed - skip
    1) https://www.python.org/downloads/ Download python from here (usually the latest)
    2) Install the exe file . When asked : click yes on add python to enviroment variables

  
    From CMD go to your directory using CD (changes depending on pc/storage place etc)
    When inside the jonidas_project folder type :
    
    python -m venv venv - only use this the first time (it creates a packaged virtual env)
    venv\Scripts\activate - This part activates the virtual env , so you dont have to install any tool
    python main.py - Runs the code

    The code will run and when it finishes (averaged 1.25 seconds per file(
    it will create 2 excel files , 1 with non normalized data, one with normalized

