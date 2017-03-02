FROM swiftdocker/swift:3.0.2

MAINTAINER muukii <m@muukii.me>

RUN apt-get update
RUN apt-get install zip unzip

RUN git clone https://github.com/apple/swift-protobuf.git
RUN swift-protobuf && swift build --configuration release

RUN curl -L https://github.com/google/protobuf/releases/download/v3.2.0/protoc-3.2.0-linux-x86_64.zip -O ./protocprotoc-3.2.0-linux-x86_64.zip
RUN unzip protocprotoc-3.2.0-linux-x86_64.zip -d ./protoc
