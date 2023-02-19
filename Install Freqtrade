https://www.freqtrade.io/en/stable/docker_quickstart/



mkdir ft_userdata
cd ft_userdata/
# Download the docker-compose file from the repository
curl https://raw.githubusercontent.com/freqtrade/freqtrade/stable/docker-compose.yml -o docker-compose.yml

# Pull the freqtrade image
docker compose pull

# Create user directory structure
docker compose run --rm freqtrade create-userdir --userdir user_data

# Create configuration - Requires answering interactive questions
docker compose run --rm freqtrade new-config --config user_data/config.json


Adding a custom strategy¶
The configuration is now available as user_data/config.json
Copy a custom strategy to the directory user_data/strategies/
Add the Strategy' class name to the docker-compose.yml file
The SampleStrategy is run by default.

# Launch the bot in trading mode (Dry-run or Live-trading, depending on your answer to the corresponding question you made above).
docker compose up -d

# You can check for running instances with:
docker compose ps

# Download the latest image
docker compose pull

# Restart the image
docker compose up -d

# Shutdown the container
docker compose down
