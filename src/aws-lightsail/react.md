## Platform: LINUX_UNIX

aws-cli lightsail get-blueprints --region "us-east-1"

### Configuration

INSTANCE_NAME="instance-$(date +%y%m%d)"

KEY_PAIR_NAME="key-pair-$(date +%y%m%d)" 

### Create LightSail key pair

aws-cli lightsail create-key-pair --key-pair-name $KEY_PAIR_NAME

### Create LightSail instance

aws-cli lightsail create-instances \
    --instance-names $INSTANCE_NAME \
    --availability-zone "us-east-1a" \
    --blueprint-id "ubuntu_20_04" \
    --bundle-id "micro_1_0"

### 

aws-cli lightsail get-instance --instance-name $INSTANCE_NAME

### 

aws-cli lightsail get-key-pair --key-pair-name <value>
