AVRCOMMON = ./../arduino_common/
SOURCES = $(AVRCOMMON)/avrdebug.cpp $(AVRCOMMON)/avrlibc_compat.cpp src/CC3000_utils.cpp
HEADERS = $(SOURCES:.cpp=.h)

all:	avrsupport.h avrsupport.cpp

avrsupport.h: $(HEADERS)
	@cat $(HEADERS) > avrsupport.h

avrsupport.cpp: $(SOURCES)
	@echo "#include \"avrsupport.h\"" > avrsupport.cpp
	@cat $(SOURCES) >> avrsupport.cpp
