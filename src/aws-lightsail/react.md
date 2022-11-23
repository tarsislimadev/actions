# AWS LightSail CLI

[CLI Docs](https://docs.aws.amazon.com/cli/latest/reference/lightsail/index.html#cli-aws-lightsail)

## Configuration

INSTANCE_NAME="instance-$(date +%y%m%d)"

KEY_PAIR_NAME="key-pair-$(date +%y%m%d)" 

## Getting blueprints

```
aws-cli lightsail get-blueprints \
    --region "us-east-1"
```

### Creating key pair

```
aws-cli lightsail create-key-pair \
    --key-pair-name $KEY_PAIR_NAME
```

### Creating instance

```
aws-cli lightsail create-instances \
    --instance-names $INSTANCE_NAME \
    --availability-zone "us-east-1a" \
    --blueprint-id "ubuntu_20_04" \
    --bundle-id "micro_1_0"
```

### Getting instance

```
aws-cli lightsail get-instance \
    --instance-name $INSTANCE_NAME
```

### Getting key pair

```
aws-cli lightsail get-key-pair \
    --key-pair-name <value>
```
