CXX  := g++
CXXFLAGS := -std=c++11

SRCDIR = .
OBJDIR = .

SRCS   = aes.cpp
TARGET = aes
OBJS   = $(addprefix $(OBJDIR)/, $(SRCS:.cpp=.o))


all: clean $(OBJS)
	$(CXX) $(CXXFLAGS) -o $(TARGET) $(OBJS)

$(OBJDIR)/%.o: $(SRCDIR)/%.cpp
	@mkdir -p $(@D)
	$(CXX) $(CXXFLAGS) -o $@ -c $<

run: all
	@./$(TARGET)

clean:
	rm -fr *.o $(OBJDIR)/*.o