KxMovie - movie player for iOS using ffmpeg (modified by kinglonghuang)
===========================================

### Download & Compile

First you need download, configure and build [FFmpeg](http://ffmpeg.org/index.html).
For this open console and type in
	
	git clone https://github.com/lvjian700/kxmovie.git
	cd kxmovie
	./install-gas.sh #use sudo command, you should input your password
	./compile-ffmpeg.sh

Notes:  
Rake file was deprecated. Do not use it.

### Usage

1. Open the kxmovie.xcodeproj with Xcode and drop the kxmovie/ffmpeg_XX into your project.
2. Set the “header search path” to your “ffmpeg_XX/include” folder, something like "$(SRCROOT)/kxmovie/ffmpeg_armv7/include"
3. Command+B, enjoy yourself :)

Note: If you want to build only the armv7 version, delete the armv7s item in the “Vaild Architectures” row, or delete the armv7 item if you want to build only a armv7 version

For play movies:

	ViewController *vc;
	vc = [KxMovieViewController movieViewControllerWithContentPath:path parameters:nil];
	[self presentViewController:vc animated:YES completion:nil];

See KxMovieExample demo project as example of using.

Also, you can include kxmovie as subproject.
Look at [kxtorrent](https://github.com/kolyvan/kxtorrent) as example.

Remember, you need to copy some movies via iTunes for playing them.
And you can use kxmovie for streaming from remote sources via rtsp,rtmp,http,etc.

### Requirements

at least iOS 5.1 and iPhone 3GS 

### Screenshots:

![movie view](https://raw.github.com/kolyvan/kxmovie/master/screenshot-movie.png "Movie View")
![info view](https://raw.github.com/kolyvan/kxmovie/master/screenshot-info.png "Info View")

### Feedback

This is forked project, you can feedback to me or other author below:	

Tweet me — [@kolyvan_ru](http://twitter.com/kolyvan_ru).
Email: kinglong_h@126.com
