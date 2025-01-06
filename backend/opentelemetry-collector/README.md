# Build OTEL COLLECTOR image for cloud run as a side car

export GCP_PROJECT=<project-id>
export REPO=<your-artifact-registry-repo-name>
export AR_REGION=<artifact-registry-region>

cd opentelemetry-collector

docker build -t $AR_REGION-docker.pkg.dev/$GCP_PROJECT/$REPO/otel-collector-metrics .
docker push $AR_REGION-docker.pkg.dev/$GCP_PROJECT/$REPO/otel-collector-metrics