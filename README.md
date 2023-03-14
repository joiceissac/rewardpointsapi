## About The Project

The api for reward calculation has done in laravel framework.
The database used for this Project is Mysql.

## Database Configuration

The database credentials have written in the .env file in the <b>rewardcalculator</b> folder

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=rewardcalculator
DB_USERNAME=admin
DB_PASSWORD=admin



## API

The route path of API set in rewardcalculator\routes\api.php file.

Eg: Route::get('rewardpoints/{customerid}', 'RewardpointsController@calculator');


The API code has written in rewardcalculator\app\Http\Controllers\RewardpointsController.php

I wrote a function named <b>calculator </b> to calculate the reward points


## API URL

Example for API Url is given below

http://127.0.0.1:8000/api/rewardpoints/1


here 127.0.0.1:8000 is the host name
the number 1 is the customer id

You can see the customer's last 3 months reward points details and its summary in the result.

Example for api response is given below:

{
    "status": "success",
    "data": {
        "transaction": [
            {
                "year_month": "2023-03",
                "rewardpoints": 340
            },
            {
                "year_month": "2023-02",
                "rewardpoints": 498
            },
            {
                "year_month": "2023-01",
                "rewardpoints": 898
            }
        ],
        "customername": "Joice",
        "totalsummarypoints": 898
    }
}


## MYSQL FILE

You can see mysql file in sql_backup folder