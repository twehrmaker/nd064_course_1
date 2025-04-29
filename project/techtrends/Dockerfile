# Use the Python 3.8 base image
FROM python:3.10-slim

# Set the working directory in the container
WORKDIR .

# Copy the requirements.txt file into the container
COPY requirements.txt .

# Install the required Python packages
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application files into the container
COPY . .

# Expose the application port
EXPOSE 3111

# Initialize the database by running init_db.py
RUN python init_db.py

# Set the default command to run the application
CMD ["python", "app.py"]