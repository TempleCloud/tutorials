
# download data files
init:
	curl -s https://archive.ics.uci.edu/ml/machine-learning-databases/iris/iris.data -o iris-data.csv
	curl -s https://archive.ics.uci.edu/ml/machine-learning-databases/iris/iris.names -o iris-data-meta.txt
	echo "sepalLength,sepalWidth,petalLength,petalWidth,species\n$$(cat iris-data.csv)" > iris-data.csv  

# run node webserver
run:
	http-server

open:
	open http://localhost:8080

stop:
	ps -lA | grep '/usr/local/bin/http-server' | head -n 1 | awk '{print $$2}' | xargs kill


