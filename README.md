import random
import time

def read_soil_moisture():
    # 실제로는 센서 값
    return random.randint(0, 100)

def water_pump(on):
    if on:
        print("💧 물 주는 중...")
    else:
        print("물 멈춤")

while True:
    moisture = read_soil_moisture()
    print(f"토양 수분: {moisture}")

    if moisture < 30:
        water_pump(True)
    else:
        water_pump(False)

    time.sleep(2)
