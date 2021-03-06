# Dquery
An API written in flask which takes GET request at /1/queries/count/<DATE_PREFIX> endpoint : returns a JSON object specifying the number of distinct query between that time interval.


## Live demo
Hosted on AWS
Change 2015 to the <date_prefix> of your choice.
http://3.109.122.49:5000/1/queries/count/2015


## Requirements
- Python 3.7.x
- Flask 2.x 
- Sqlite 3

## Installation

```sh
git clone https://github.com/dasagreeva/query.git
cd dquery 
```

### Running with Gunicorn
```
pip install -r requirements.txt
pip install gunicorn
gunicorn --bind 0.0.0.0:5000 api:app
```

### Download Database
Have to download a Database in Repository to use this API.
[Drive Database Link](https://drive.google.com/file/d/1lvrpSmp6CS-fp6ySVREzzEETLXSaZ7of/view?usp=sharing)


## Usage
After running the server on some port (it use port =5000= by default).
Send a POST request using =curl=.
```sh
curl https://localhost:5000/1/queries/count/2015-08-03
{"count": 3}
```
