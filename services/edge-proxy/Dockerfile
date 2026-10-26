FROM envoyproxy/envoy:v1.31.2@sha256:7b4ce7b1c8a5e4b4f4f0c2d6a3a1c6f9a8d2e3b4c5d6e7f8091a2b3c4d5e6f70

COPY envoy.yaml /etc/envoy/envoy.yaml
EXPOSE 10000 9901
CMD ["envoy", "-c", "/etc/envoy/envoy.yaml", "--log-level", "info"]
