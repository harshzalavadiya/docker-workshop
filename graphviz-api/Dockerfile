FROM python
ADD api.py .
ADD requirements.txt .
RUN pip install -r requirements.txt
RUN apt-get update
RUN apt-get install -y graphviz
CMD ["gunicorn", "-w","4","api:app","-b","0.0.0.0:8000"]
