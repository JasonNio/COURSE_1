FROM python:3.8  
  
WORKDIR /app  
  
COPY ./techtrends/requirements.txt ./  
  
RUN pip install --no-cache-dir -r requirements.txt  
  
COPY . .  

WORKDIR /app/techtrends

RUN python ./init_db.py  
  
EXPOSE 3111  
  
CMD ["python", "app.py"]  