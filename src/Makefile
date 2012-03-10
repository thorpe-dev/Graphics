CC      = c++
LD      = c++

CFLAGS  = -Wall -O2 -I. -c

LDFLAGS = -lm

INCS = hit.h image.h ray.h scene_parser.h vectors.h \
	object3d.h group.h camera.h orthographic_camera.h

OBJS =	image.o \
	scene_parser.o \
	sphere.o \
	group.o \
	orthographic_camera.o \
	raycast.o

all: raycast

clean:
	rm -rf $(OBJS) raycast

image.o: $(INCS) image.cc
	$(CC) $(CFLAGS) image.cc -o image.o

orthographic_camera.o: $(INCS) orthographic_camera.cc
	$(CC) $(CFLAGS) orthographic_camera.cc -o orthographic_camera.o

scene_parser.o: $(INCS) scene_parser.cc
	$(CC) $(CFLAGS) scene_parser.cc -o scene_parser.o

sphere.o: $(INCS) sphere.cc
	$(CC) $(CFLAGS) sphere.cc -o sphere.o

group.o: $(INCS) group.cc
	$(CC) $(CFLAGS) group.cc -o group.o

raycast.o: $(INCS) raycast.cc
	$(CC) $(CFLAGS) raycast.cc -o raycast.o

raycast: $(OBJS)
	$(LD) $(OBJS) -o raycast $(LDFLAGS)
