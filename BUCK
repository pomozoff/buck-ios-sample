apple_resource(
    name = 'AppResources',
    dirs = [],
    files = glob(['App/*.png']),
)

apple_binary(
    name = 'AppBinary',
    srcs = [
        'App/App.m',
        'App/Empty.swift',
    ],
    headers = ['App/App.h'],
    frameworks = [
        '$SDKROOT/System/Library/Frameworks/Foundation.framework',
        '$SDKROOT/System/Library/Frameworks/UIKit.framework',
    ],
)

apple_bundle(
    name = 'App',
    binary = ':AppBinary',
    deps = [':AppResources'],
    tests = [':AppTest'],
    extension = 'app',
    info_plist = 'App/App.plist',
)

apple_test(
    name = 'AppTest',
    test_host_app = ':App',
    srcs = [
        'Test/AppTest.m',
        'Test/Empty.swift',
    ],
    info_plist = 'Test/AppTest.plist',
    frameworks = [
        '$SDKROOT/System/Library/Frameworks/Foundation.framework',
        '$SDKROOT/System/Library/Frameworks/UIKit.framework',
        '$PLATFORM_DIR/Developer/Library/Frameworks/XCTest.framework',
    ],
)
