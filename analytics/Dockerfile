FROM python:3.14-slim-bookworm

WORKDIR /app

# Copy dependency file first so Docker can cache package installation.
COPY requirements.txt .

# Install Python dependencies needed by the Flask analytics application.
RUN pip install --no-cache-dir -r requirements.txt

# Copy the application source code into the container.
COPY . .

EXPOSE 5153

CMD ["python", "app.py"]