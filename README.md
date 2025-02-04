# Run

```
pipenv sync
pipenv run opentelemetry-instrument uvicorn ui.main:app --proxy-headers --host=0.0.0.0 --port=5000 --log-level=error
```

# Gen Traffic
```
curl http://localhost:5000                                                 
{"message":"Hello World"} 
curl http://localhost:5000
{"message":"Hello World"}
```

# Metrics

```
curl http://localhost:9464/metrics 
```