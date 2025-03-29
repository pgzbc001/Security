# Generate a Least Privilege IAM Policy Based on Access Patterns
sed -e "s/BUCKET_NAME/awscookbook903-$RANDOM_STRING/g" \
-e "s|AWS_ACCOUNT_ID|${AWS_ACCOUNT_ID}|g" \
cloudtrail-s3policy-template.json > cloudtrail-s3policy.json
## Clean up 
### Delete the IAM policy that you created
