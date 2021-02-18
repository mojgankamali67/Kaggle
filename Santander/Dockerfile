FROM python:3.7

RUN pip3 install jupyter pandas numpy matplotlib seaborn lightgbm scikit-learn 

WORKDIR /usr/src/app
COPY data data

#to circumvent githubs file size limit, we had to break the dataset into chunks
#now we merge them again
RUN cat train.csv.* > train.csv 
RUN rm train.csv.*
COPY Santander.ipynb .

CMD ["jupyter", "notebook", "--port=8888", "--no-browser", "--ip=0.0.0.0", "--allow-root", "--NotebookApp.token=''", "--NotebookApp.password=''"]
