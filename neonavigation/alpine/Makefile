.PHONY: all
all:
	docker build --cache-from alpineros/alpine-ros:melodic-ros-core -t demo-alpine-ros .

.PHONY: clean
clean:
	docker system prune -f
