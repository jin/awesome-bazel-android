android_sdk_repository(
    name = "androidsdk",
    api_level = 28,
    build_tools_version = "28.0.3",
)

android_ndk_repository(
    name = "androidndk",
)

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

# https://github.com/square/bazel_maven_repository
MAVEN_REPOSITORY_RULES_VERSION = "1.0-rc6"
MAVEN_REPOSITORY_RULES_SHA = "e29e57beef25e771acbeddd17b9b9c53d40f81a438018197110f5c2896682e3b"
http_archive(
    name = "maven_repository_rules",
    urls = ["https://github.com/square/bazel_maven_repository/archive/%s.zip" % MAVEN_REPOSITORY_RULES_VERSION],
    type = "zip",
    strip_prefix = "bazel_maven_repository-%s" % MAVEN_REPOSITORY_RULES_VERSION,
    sha256 = MAVEN_REPOSITORY_RULES_SHA,
)
load("@maven_repository_rules//maven:maven.bzl", "maven_repository_specification")
maven_repository_specification(
    name = "maven",
    repository_urls = [
        "https://repo1.maven.org/maven2",
        "https://dl.google.com/dl/android/maven2",
    ],
    artifacts = {
        "com.google.guava:guava:25.0-jre": { "insecure": True },
        "com.google.code.findbugs:jsr305:3.0.1": { "insecure": True },
        "com.google.errorprone:error_prone_annotations:2.1.3": { "insecure": True },
        "com.google.j2objc:j2objc-annotations:1.1": { "insecure": True },
        "org.checkerframework:checker-compat-qual:2.0.0": { "insecure": True },
        "org.codehaus.mojo:animal-sniffer-annotations:1.14": { "insecure": True },

        "com.github.bumptech.glide:glide:4.9.0:aar": { "insecure": True },
        "com.github.bumptech.glide:gifdecoder:4.9.0:aar": { "insecure": True },
        "com.github.bumptech.glide:disklrucache:4.9.0": { "insecure": True },
        "com.github.bumptech.glide:annotations:4.9.0": { "insecure": True },
        "com.android.support:animated-vector-drawable:27.1.1:aar": { "insecure": True },
        "com.android.support:support-annotations:27.1.1": { "insecure": True },
        "com.android.support:support-compat:27.1.1:aar": { "insecure": True },
        "com.android.support:support-core-ui:27.1.1:aar": { "insecure": True },
        "com.android.support:support-core-utils:27.1.1:aar": { "insecure": True },
        "com.android.support:support-fragment:27.1.1:aar": { "insecure": True },
        "com.android.support:support-vector-drawable:27.1.1:aar": { "insecure": True },
        "android.arch.lifecycle:livedata-core:1.1.0:aar": { "insecure": True },
        "android.arch.lifecycle:runtime:1.1.0:aar": { "insecure": True },
        "android.arch.lifecycle:viewmodel:1.1.0:aar": { "insecure": True },
        "android.arch.lifecycle:common:1.1.0": { "insecure": True },
        "android.arch.core:common:1.1.0": { "insecure": True },
        "android.arch.core:runtime:1.1.0:aar": { "insecure": True },
    },
)

