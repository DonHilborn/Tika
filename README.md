# Tika
mkdir /usr/local/apache-maven
cd /usr/local/apache-maven
wget http://mirror.nexcess.net/apache/maven/maven-3/3.3.3/binaries/apache-maven-3.3.3-bin.tar.gz
tar -zxvf apache-maven-3.3.3-bin.tar.gz

# Where,

# -z : Work on gzip compression automatically when reading archives.
# -x : Extract archives.
# -v : Produce verbose output i.e. display progress and extracted file list on screen.
# -f : Read the archive from the archive to the specified file. In this example, read backups.tar.gz archive.
# -t : List the files in the archive.

vi /etc/profile

export PATH=$PATH:/usr/local/apache-maven/apache-maven-3.3.3/bin
export MAVEN_OPTS="-Xms256m -Xmx512m"

source /etc/profile

echo $JAVA_HOME
/usr/lib/jvm/java-1.7.0-openjdk.x86_64

mkdir /usr/bin/tika
cd /usr/bin/tika

wget http://mirrors.sonic.net/apache/tika/tika-1.8-src.zip

unzip tika-1.8-src.zip

rm tika-1.8-src.zip

/usr/bin/tika/tika-1.8

mvn install
