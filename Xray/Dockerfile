FROM python:3.7

RUN pip3 install jupyter pandas numpy matplotlib seaborn tensorflow keras scikit-learn 

WORKDIR /usr/src/app
COPY data data
COPY Xray.ipynb .

CMD ["jupyter", "notebook", "--port=8888", "--no-browser", "--ip=0.0.0.0", "--allow-root", "--NotebookApp.token=''", "--NotebookApp.password=''"]