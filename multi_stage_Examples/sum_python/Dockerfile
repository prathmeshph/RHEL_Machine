# First stage: Copy application code
FROM python as builder

WORKDIR /python_app

COPY . /python_app

# Final stage: Run the application
FROM gcr.io/distroless/python3-debian10

WORKDIR /python_app

# Copy application code from the builder stage
COPY --from=builder /python_app /python_app

# Command to run the application
CMD ["python", "it.py"]
