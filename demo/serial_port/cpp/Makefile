# Makefile

RM = rm -f
CXX = arm-linux-g++
CXXFLAGS = -Wall -g -static
INCLUDE = 
LDFLAGS = -static
LDPATH = 

OBJS = error.o wraptermios.o wrapsock.o
PROGS =	tty_open tty_open_easy tty_set_speed tty_set_parity tty_set_timeout \
		tty_read tty_write tty_read_select tty_read_poll tty_read_epoll \
		tty_read2 tty_read_poll2 tty_set_dsr tty_test_dsr

.PHONY: all
all: $(PROGS)
	@echo "build OK!"

clean:
	@$(RM) $(PROGS) *.o
	@echo "clean OK!"

%.o:%.cpp
	$(CXX) -o $@ -c $< $(CXXFLAGS) $(INCLUDE)

tty_open: tty_open.o $(OBJS)
	$(CXX) -o $@ $^ $(LDFLAGS) $(LDPATH)

tty_open_easy: tty_open_easy.o $(OBJS)
	$(CXX) -o $@ $^ $(LDFLAGS) $(LDPATH)

tty_set_speed: tty_set_speed.o $(OBJS)
	$(CXX) -o $@ $^ $(LDFLAGS) $(LDPATH)

tty_set_parity: tty_set_parity.o $(OBJS)
	$(CXX) -o $@ $^ $(LDFLAGS) $(LDPATH)

tty_set_timeout: tty_set_timeout.o $(OBJS)
	$(CXX) -o $@ $^ $(LDFLAGS) $(LDPATH)

tty_read: tty_read.o $(OBJS)
	$(CXX) -o $@ $^ $(LDFLAGS) $(LDPATH)

tty_write: tty_write.o $(OBJS)
	$(CXX) -o $@ $^ $(LDFLAGS) $(LDPATH)

tty_read_select: tty_read_select.o $(OBJS)
	$(CXX) -o $@ $^ $(LDFLAGS) $(LDPATH)

tty_read_poll: tty_read_poll.o $(OBJS)
	$(CXX) -o $@ $^ $(LDFLAGS) $(LDPATH)

tty_read_epoll: tty_read_epoll.o $(OBJS)
	$(CXX) -o $@ $^ $(LDFLAGS) $(LDPATH)

tty_read2: tty_read2.o $(OBJS) tty_reader.o
	$(CXX) -o $@ $^ $(LDFLAGS) $(LDPATH)

tty_read_poll2: tty_read_poll2.o $(OBJS) tty_reader.o
	$(CXX) -o $@ $^ $(LDFLAGS) $(LDPATH)

tty_set_dsr: tty_set_dsr.o $(OBJS)
	$(CXX) -o $@ $^ $(LDFLAGS) $(LDPATH)

tty_test_dsr: tty_test_dsr.o $(OBJS)
	$(CXX) -o $@ $^ $(LDFLAGS) $(LDPATH)

