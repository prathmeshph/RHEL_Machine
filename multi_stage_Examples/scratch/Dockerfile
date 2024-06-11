# First stage: Copy application code
FROM python as builder

WORKDIR /python_app

COPY . /python_app

# Final stage: Run the application
FROM scratch

WORKDIR /python_app

# Copy application code from the builder stage
COPY --from=builder /python_app /python_app

# Set environment variables if needed
# ENV MY_ENV_VAR=my_value

# Command to run the application
CMD ["python", "it.py"]

