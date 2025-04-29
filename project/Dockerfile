# Use the Python 3.10 base image
FROM python:3.10-slim


# Copy the files into the container
COPY ./techtrends ./dist

# Set the working directory in the container
WORKDIR ./dist

# Install the required Python packages
RUN pip install --no-cache-dir -r requirements.txt

# Initialize the database by running init_db.py
RUN python init_db.py

# Expose the application port
EXPOSE 3111

# Set the default command to run the application
CMD ["python", "app.py"]