PORTNAME=	gitoxide
DISTVERSIONPREFIX=	git-repository-v
DISTVERSION=	0.32.0
PORTREVISION=	8
CATEGORIES=	devel

MAINTAINER=	yuri@FreeBSD.org
COMMENT=	Idiomatic, lean, fast & safe pure Rust implementation of Git
WWW=		https://github.com/Byron/gitoxide

LICENSE=	APACHE20 MIT
LICENSE_COMB=	dual
LICENSE_FILE_APACHE20=	${WRKSRC}/LICENSE-APACHE
LICENSE_FILE_MIT=	${WRKSRC}/LICENSE-MIT

LIB_DEPENDS=	libcurl.so:ftp/curl

USES=		cargo

USE_GITHUB=	yes
GH_ACCOUNT=	Byron

CARGO_CRATES=	adler-1.0.2 \
		ahash-0.8.2 \
		aho-corasick-0.7.20 \
		anes-0.1.6 \
		ansi_term-0.12.1 \
		anyhow-1.0.68 \
		arc-swap-1.6.0 \
		arrayvec-0.7.2 \
		async-attributes-1.1.2 \
		async-channel-1.8.0 \
		async-executor-1.5.0 \
		async-global-executor-2.3.1 \
		async-io-1.12.0 \
		async-lock-2.6.0 \
		async-net-1.7.0 \
		async-std-1.12.0 \
		async-task-4.3.0 \
		async-trait-0.1.60 \
		atoi-2.0.0 \
		atomic-waker-1.0.0 \
		atty-0.2.14 \
		autocfg-1.1.0 \
		base64-0.13.1 \
		bitflags-1.3.2 \
		block-buffer-0.10.3 \
		blocking-1.3.0 \
		bstr-1.1.0 \
		btoi-0.4.2 \
		bumpalo-3.11.1 \
		bytecount-0.6.3 \
		bytes-1.3.0 \
		bytesize-1.1.0 \
		camino-1.1.1 \
		cargo-platform-0.1.2 \
		cargo_metadata-0.15.2 \
		cargo_toml-0.11.8 \
		cassowary-0.3.0 \
		cast-0.3.0 \
		castaway-0.2.2 \
		cc-1.0.78 \
		cfg-if-1.0.0 \
		ciborium-0.2.0 \
		ciborium-io-0.2.0 \
		ciborium-ll-0.2.0 \
		clap-3.2.23 \
		clap_derive-3.2.18 \
		clap_lex-0.2.4 \
		clru-0.6.1 \
		cmake-0.1.49 \
		combine-4.6.6 \
		compact_str-0.6.1 \
		concurrent-queue-2.0.0 \
		conpty-0.3.0 \
		console-0.15.3 \
		core-foundation-0.9.3 \
		core-foundation-sys-0.8.3 \
		cpufeatures-0.2.5 \
		crates-index-0.18.11 \
		crc-3.0.0 \
		crc-catalog-2.1.0 \
		crc32fast-1.3.2 \
		criterion-0.4.0 \
		criterion-plot-0.5.0 \
		crossbeam-0.8.2 \
		crossbeam-channel-0.5.6 \
		crossbeam-deque-0.8.2 \
		crossbeam-epoch-0.9.13 \
		crossbeam-queue-0.3.8 \
		crossbeam-utils-0.8.14 \
		crossterm-0.25.0 \
		crossterm_winapi-0.9.0 \
		crosstermion-0.10.1 \
		crypto-common-0.1.6 \
		ctor-0.1.26 \
		curl-0.4.44 \
		curl-sys-0.4.59+curl-7.86.0 \
		dashmap-5.4.0 \
		data-encoding-2.3.3 \
		defer-0.1.0 \
		diff-0.1.13 \
		digest-0.10.6 \
		dirs-4.0.0 \
		dirs-sys-0.3.7 \
		doc-comment-0.3.3 \
		document-features-0.2.7 \
		either-1.8.0 \
		encode_unicode-0.3.6 \
		encoding_rs-0.8.31 \
		enum-as-inner-0.5.1 \
		env_logger-0.9.3 \
		env_logger-0.10.0 \
		errno-0.2.8 \
		errno-dragonfly-0.1.2 \
		event-listener-2.5.3 \
		expectrl-0.5.2 \
		fastrand-1.8.0 \
		filetime-0.2.19 \
		flate2-1.0.25 \
		fnv-1.0.7 \
		foreign-types-0.3.2 \
		foreign-types-shared-0.1.1 \
		form_urlencoded-1.1.0 \
		fs-err-2.9.0 \
		fs_extra-1.2.0 \
		futures-0.3.25 \
		futures-channel-0.3.25 \
		futures-core-0.3.25 \
		futures-executor-0.3.25 \
		futures-io-0.3.25 \
		futures-lite-1.12.0 \
		futures-sink-0.3.25 \
		futures-task-0.3.25 \
		futures-util-0.3.25 \
		generic-array-0.14.6 \
		getopts-0.2.21 \
		getrandom-0.2.8 \
		git-conventional-0.12.1 \
		git2-0.15.0 \
		gloo-timers-0.2.5 \
		h2-0.3.15 \
		half-1.8.2 \
		hashbrown-0.12.3 \
		hashbrown-0.13.1 \
		heck-0.4.0 \
		hermit-abi-0.1.19 \
		hermit-abi-0.2.6 \
		hex-0.4.3 \
		home-0.5.4 \
		hostname-0.3.1 \
		http-0.2.8 \
		http-body-0.4.5 \
		httparse-1.8.0 \
		httpdate-1.0.2 \
		human_format-1.0.3 \
		humantime-2.1.0 \
		hyper-0.14.23 \
		hyper-rustls-0.23.2 \
		hyper-tls-0.5.0 \
		idna-0.2.3 \
		idna-0.3.0 \
		imara-diff-0.1.5 \
		indexmap-1.9.2 \
		insta-1.23.0 \
		instant-0.1.12 \
		io-close-0.3.7 \
		io-lifetimes-1.0.3 \
		ipconfig-0.3.1 \
		ipnet-2.7.0 \
		is-terminal-0.4.2 \
		is_ci-1.1.1 \
		itertools-0.10.5 \
		itoa-1.0.5 \
		jobserver-0.1.25 \
		js-sys-0.3.60 \
		jwalk-0.8.1 \
		kv-log-macro-1.0.7 \
		lazy_static-1.4.0 \
		libc-0.2.139 \
		libgit2-sys-0.14.0+1.5.0 \
		libz-ng-sys-1.1.8 \
		libz-sys-1.1.8 \
		linked-hash-map-0.5.6 \
		linux-raw-sys-0.1.4 \
		litrs-0.2.3 \
		lock_api-0.4.9 \
		log-0.4.17 \
		lru-cache-0.1.2 \
		lzma-sys-0.1.20 \
		maplit-1.0.2 \
		match_cfg-0.1.0 \
		matches-0.1.9 \
		maybe-async-0.2.6 \
		memchr-2.5.0 \
		memmap2-0.5.8 \
		memoffset-0.6.5 \
		memoffset-0.7.1 \
		mime-0.3.16 \
		mime_guess-2.0.4 \
		minimal-lexical-0.2.1 \
		miniz_oxide-0.6.2 \
		mio-0.8.5 \
		native-tls-0.2.11 \
		nix-0.21.0 \
		nix-0.23.2 \
		nix-0.26.1 \
		nom-7.1.1 \
		num-traits-0.2.15 \
		num_cpus-1.15.0 \
		num_threads-0.1.6 \
		once_cell-1.17.0 \
		oorandom-11.1.3 \
		openssl-0.10.45 \
		openssl-macros-0.1.0 \
		openssl-probe-0.1.5 \
		openssl-sys-0.9.80 \
		os_str_bytes-6.4.1 \
		output_vt100-0.1.3 \
		owo-colors-3.5.0 \
		papergrid-0.5.1 \
		parking-2.0.0 \
		parking_lot-0.11.2 \
		parking_lot-0.12.1 \
		parking_lot_core-0.8.6 \
		parking_lot_core-0.9.5 \
		percent-encoding-2.2.0 \
		pin-project-lite-0.2.9 \
		pin-utils-0.1.0 \
		pkg-config-0.3.26 \
		plotters-0.3.4 \
		plotters-backend-0.3.4 \
		plotters-svg-0.3.3 \
		polling-2.5.2 \
		ppv-lite86-0.2.17 \
		pretty_assertions-1.3.0 \
		proc-macro-error-1.0.4 \
		proc-macro-error-attr-1.0.4 \
		proc-macro2-1.0.49 \
		prodash-23.0.0 \
		ptyprocess-0.3.0 \
		pulldown-cmark-0.9.2 \
		quick-error-1.2.3 \
		quick-error-2.0.1 \
		quote-1.0.23 \
		rand-0.8.5 \
		rand_chacha-0.3.1 \
		rand_core-0.6.4 \
		rayon-1.6.1 \
		rayon-core-1.10.1 \
		redox_syscall-0.2.16 \
		redox_users-0.4.3 \
		regex-1.7.0 \
		regex-automata-0.1.10 \
		regex-syntax-0.6.28 \
		remove_dir_all-0.5.3 \
		reqwest-0.11.13 \
		resolv-conf-0.7.0 \
		ring-0.16.20 \
		rustc-hash-1.1.0 \
		rustix-0.36.6 \
		rustls-0.20.7 \
		rustls-pemfile-1.0.1 \
		rustversion-1.0.11 \
		ryu-1.0.12 \
		same-file-1.0.6 \
		schannel-0.1.20 \
		scopeguard-1.1.0 \
		sct-0.7.0 \
		security-framework-2.7.0 \
		security-framework-sys-2.6.1 \
		semver-1.0.16 \
		serde-1.0.152 \
		serde_derive-1.0.152 \
		serde_json-1.0.91 \
		serde_urlencoded-0.7.1 \
		serial_test-0.9.0 \
		serial_test_derive-0.9.0 \
		sha1-0.10.5 \
		sha1-asm-0.5.1 \
		sha1_smol-1.0.0 \
		signal-hook-0.3.14 \
		signal-hook-mio-0.2.3 \
		signal-hook-registry-1.4.0 \
		similar-2.2.1 \
		slab-0.4.7 \
		smallvec-1.10.0 \
		smartstring-1.0.1 \
		socket2-0.4.7 \
		spin-0.5.2 \
		static_assertions-1.1.0 \
		strsim-0.10.0 \
		symlink-0.1.0 \
		syn-1.0.107 \
		tabled-0.8.0 \
		tar-0.4.38 \
		tempfile-3.3.0 \
		termcolor-1.1.3 \
		textwrap-0.16.0 \
		thiserror-1.0.38 \
		thiserror-impl-1.0.38 \
		time-0.3.17 \
		time-core-0.1.0 \
		time-macros-0.2.6 \
		tinytemplate-1.2.1 \
		tinyvec-1.6.0 \
		tinyvec_macros-0.1.0 \
		tokio-1.23.0 \
		tokio-native-tls-0.3.0 \
		tokio-rustls-0.23.4 \
		tokio-util-0.7.4 \
		toml-0.5.10 \
		toml_edit-0.14.4 \
		tower-service-0.3.2 \
		tracing-0.1.37 \
		tracing-attributes-0.1.23 \
		tracing-core-0.1.30 \
		trust-dns-proto-0.22.0 \
		trust-dns-resolver-0.22.0 \
		try-lock-0.2.3 \
		tui-0.19.0 \
		tui-react-0.19.0 \
		typenum-1.16.0 \
		uluru-3.0.0 \
		unicase-2.6.0 \
		unicode-bidi-0.3.8 \
		unicode-bom-1.1.4 \
		unicode-ident-1.0.6 \
		unicode-normalization-0.1.22 \
		unicode-segmentation-1.10.0 \
		unicode-width-0.1.10 \
		untrusted-0.7.1 \
		url-2.3.1 \
		value-bag-1.0.0-alpha.9 \
		vcpkg-0.2.15 \
		version_check-0.9.4 \
		waker-fn-1.1.0 \
		walkdir-2.3.2 \
		want-0.3.0 \
		wasi-0.11.0+wasi-snapshot-preview1 \
		wasm-bindgen-0.2.83 \
		wasm-bindgen-backend-0.2.83 \
		wasm-bindgen-futures-0.4.33 \
		wasm-bindgen-macro-0.2.83 \
		wasm-bindgen-macro-support-0.2.83 \
		wasm-bindgen-shared-0.2.83 \
		web-sys-0.3.60 \
		webpki-0.22.0 \
		webpki-roots-0.22.6 \
		wepoll-ffi-0.1.2 \
		widestring-0.5.1 \
		winapi-0.3.9 \
		winapi-i686-pc-windows-gnu-0.4.0 \
		winapi-util-0.1.5 \
		winapi-x86_64-pc-windows-gnu-0.4.0 \
		windows-0.29.0 \
		windows-0.40.0 \
		windows-sys-0.36.1 \
		windows-sys-0.42.0 \
		windows_aarch64_gnullvm-0.40.0 \
		windows_aarch64_gnullvm-0.42.0 \
		windows_aarch64_msvc-0.29.0 \
		windows_aarch64_msvc-0.36.1 \
		windows_aarch64_msvc-0.40.0 \
		windows_aarch64_msvc-0.42.0 \
		windows_i686_gnu-0.29.0 \
		windows_i686_gnu-0.36.1 \
		windows_i686_gnu-0.40.0 \
		windows_i686_gnu-0.42.0 \
		windows_i686_msvc-0.29.0 \
		windows_i686_msvc-0.36.1 \
		windows_i686_msvc-0.40.0 \
		windows_i686_msvc-0.42.0 \
		windows_x86_64_gnu-0.29.0 \
		windows_x86_64_gnu-0.36.1 \
		windows_x86_64_gnu-0.40.0 \
		windows_x86_64_gnu-0.42.0 \
		windows_x86_64_gnullvm-0.40.0 \
		windows_x86_64_gnullvm-0.42.0 \
		windows_x86_64_msvc-0.29.0 \
		windows_x86_64_msvc-0.36.1 \
		windows_x86_64_msvc-0.40.0 \
		windows_x86_64_msvc-0.42.0 \
		winreg-0.10.1 \
		xz2-0.1.7 \
		yaml-rust-0.4.5 \
		yansi-0.5.1

OPENSSLINC=	/usr/include
OPENSSLLIB=	/usr/lib

PLIST_FILES=	bin/ein \
		bin/gix

PORTSCOUT=	ignore:1 # repository tags don't make sense and only cause confusion

post-install:
	@${STRIP_CMD} \
		${STAGEDIR}${PREFIX}/bin/ein \
		${STAGEDIR}${PREFIX}/bin/gix

.include <bsd.port.mk>
