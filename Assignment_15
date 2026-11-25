import gc
import sys

def create_objects():
    data = []
    for i in range(1000):
        data.append([i] * 100)
    return data


def display_memory(data):
    print("Memory used:", sys.getsizeof(data), "bytes")


print("Initial Garbage Collection Count:", gc.get_count())

objects = create_objects()
print("\nAfter creating objects:")
display_memory(objects)

gc.set_debug(gc.DEBUG_STATS)

del objects

print("\nGarbage Collection Started:")
collected = gc.collect()

print("Garbage collector collected", collected, "objects.")

print("\nFinal Garbage Collection Count:", gc.get_count())

gc.set_debug(0)

print("\nGarbage Collection Completed.")
