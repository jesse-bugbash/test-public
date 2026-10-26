FROM python:3.10-slim

# Old-style LABEL with a stale value from before the repo moved.
LABEL org.opencontainers.image.source https://github.com/example-shop-legacy/reports

WORKDIR /job
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
COPY reports ./reports
CMD ["python", "-m", "reports.nightly"]
