FROM python:3.10-alpine
WORKDIR /app
RUN apk add --no-cache gcc musl-dev linux-headers
COPY requirements.txt .  
RUN pip install --no-cache-dir -r requirements.txt  
COPY . .  
EXPOSE 9000
CMD ["flask", "run", "--host=0.0.0.0", "--port=9000", "--debug"]
