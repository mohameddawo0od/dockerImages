FROM openjdk:8-jdk

RUN apt-get update
RUN apt-get install -y ant
RUN echo $JAVA_HOME
RUN apt-get install -y wget
RUN apt-get install -y cmake
RUN apt-get install -y g++
RUN apt-get install -y unzip
RUN apt-get install -y vim
RUN java -version
RUN apt-get install -y build-essential


#RUN mkdir /opencv && \
 #   cd /opencv && \
  #  git clone https://github.com/opencv/opencv.git && \
   # cd opencv && \
    #git checkout 4.3.0

#RUN cd /opencv/opencv && \
 #   mkdir build && \
  #  cd build && \
   # cmake -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr/local .. && \
    #make -j$(nproc) && \
    #make install


# Set the Java classpath for OpenCV
#ENV CLASSPATH /usr/local/share/java/opencv4

# Verify OpenCV installation
#RUN java -cp $CLASSPATH -XshowSettings:properties -version

RUN apt-get install -y \
    m4 \
    autoconf \
    automake \
    libtool \
    pkg-config \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

#RUN wget https://github.com/DanBloomberg/leptonica/releases/download/1.82.0/leptonica-1.82.0.tar.gz \
 #   && tar -zxvf leptonica-1.82.0.tar.gz \
  #  && cd leptonica-1.82.0 \
   # && ./autogen.sh \
    #&& ./configure \
    #&& make \
    #&& make install \
    #&& ldconfig \
    #&& cd .. \
    #&& rm -rf leptonica-1.82.0 leptonica-1.82.0.tar.gz

#RUN wget https://github.com/tesseract-ocr/tesseract/archive/refs/tags/5.2.0.tar.gz \
 #   && tar -zxvf 5.2.0.tar.gz \
 #   && cd tesseract-5.2.0 \
 #   && ./autogen.sh \
 #   && ./configure \
  #  && make \
  #  && make install \
   # && ldconfig \
   # && cd ../.. \
   # && rm -rf tesseract-5.2.0 5.2.0.tar.gz


RUN mkdir -p /usr/local/share/tessdata/

# Download e13b language data
RUN wget -O /usr/local/share/tessdata/e13b.traineddata \
    https://github.com/DoubangoTelecom/tesseractMICR/tree/master/tessdata_best/e13b.traineddata

# Download ocr_int language data
RUN wget -O /usr/local/share/tessdata/ocrb_int.traineddata \
    https://github.com/Shreeshrii/tessdata_ocrb/blob/master/ocrb_int.traineddata

