import logging

logging.basicConfig(
    level=logging.DEBUG,
    format="%(asctime)s - %(levelname)s - %(message)s",
    datefmt="%Y-%m-%d %H:%M",
    handlers=[
        logging.FileHandler("app.log", mode="a"),
        logging.StreamHandler()
    ]
)

logging.debug("This is a debug message")
logging.info("Program started successfully")
logging.warning("This is a warning message")
logging.error("An error occurred")
logging.critical("Critical error occurred")

print("Logging completed successfully.")
