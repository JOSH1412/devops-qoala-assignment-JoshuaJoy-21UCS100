FROM python:3.9

# FIXED: Corrected working directory from /appp to /app
WORKDIR /app

# FIXED: Fixed path 
COPY app.py /app

# FIXED: Corrected package name from 'netiface' to 'netifaces'
RUN pip install flask netifaces

# FIXED: Changed "eight thousand" to numeric 8000
EXPOSE 8000

# FIXED: Corrected typo in command from "pythn" to "python"
CMD ["python", "app.py"]
