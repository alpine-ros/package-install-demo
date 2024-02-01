.PHONY: all
all:
	docker build --cache-from ghcr.io/alpine-ros/alpine-ros:noetic-3.17-ros-core -t demo-alpine-ros .

.PHONY: clean
clean:
	docker system prune -f
