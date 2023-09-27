aws dynamodb create-table \
  --table-name test-bucket4j-local \
  --attribute-definitions AttributeName=key,AttributeType=S \
  --key-schema AttributeName=key,KeyType=HASH \
  --provisioned-throughput ReadCapacityUnits=5,WriteCapacityUnits=5 \
  --endpoint-url http://localhost:8000
  
  
aws dynamodb list-tables --endpoint-url http://localhost:8000

aws dynamodb scan --table-name my-table --endpoint-url http://localhost:8000