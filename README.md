# docker-base-images

Alpine-based docker dev base images for upcoming 0.3.0.2+ build

Warning, these are **EXPERIMENTAL** images and there might be problems with resulting binaries.

    docker run --rm -it -e CCACHE_DIR=/ccache -v /path/to/catapult-src:/catapult-src -v /path/to/ccache-output:/ccache -v /path/to/binaries-output:/binaries techbureau/dev-base-image /bin/ash
    # cd /binaries
    # ccache -s
    # cmake -DCMAKE_BUILD_TYPE=RelWithDebugInfo -G Ninja /catapult-src
    # ninja publish
    # ninja -j 6   # where 6 is number of CPUs to make parallel build


