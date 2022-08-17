# Problem statement


Pull the Python 3.8 image and keep track the number of layers it has fetched.

Create a Docker volume named app_files.

Create a container named ‘first_container’ from the Python 3.8 image with app_files volume attached to it.

Write a Python program named ‘current_time.py’ to display the current timestamp inside the app_files volume.

Create another container named ‘second_container’ from the Python 3.8 image and update the Python script located in ‘app_files’ volume to print the current date.

## Solution

1. 
```
docker pull python:3.8
```

2. 
```
docker volume create app_files
```

3. 
```
docker run -it --name <name-of-the-container> -v <volume>:<container-path> <image> <command>
dc run -it --name "first_container" -v /userPath/app_files:/app_files python:3.8 bash

```

4. 
```
cd app_files && touch create_time.py

apt update && apt install nano

pip install pytz

nano create_time.py

    import datetime, pytz

    current_time = datetime.datetime.now(pytz.timezone('Asia/Kolkata')).strftime("%H:%M:%S %z")

    print(current_time)

python create_time.py
```

5. 
```
docker run -it --name "second_container" -v /path/app_files:/app_files python:3.8 bash
```