.PHONY: all
all:
	docker build --cache-from ros:melodic-ros-core -t demo-ubuntu-ros .

.PHONY: clean
clean:
	docker system prune -f
