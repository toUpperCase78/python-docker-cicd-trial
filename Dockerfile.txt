FROM scratch
WORKDIR /app
COPY . .
CMD ["python3", "app.py"]