# Flask App

A simple Flask web application.

## Running with Docker

1. **Build the Docker image:**
	```sh
	docker build -t dockerhw .
	```

2. **Run the Docker container:**
	```sh
	docker run -p 5000:5000 dockerhw
	```

3. **Access the app:**  
	Open [http://localhost:5000](http://localhost:5000) in your browser.

---

## Running with Kubernetes

1. **Build the Docker image (if not already built):**
	```sh
	docker build -t dockerhw .
	```

2. **Deploy to Kubernetes:**
	```sh
	kubectl apply -f k8s-flask-app.yaml
	```

3. **Port-forward to access the app:**
	```sh
	kubectl port-forward service/flask-app-service 5000:5000
	```

4. **Access the app:**  
	Open [http://localhost:5000](http://localhost:5000) in your browser.