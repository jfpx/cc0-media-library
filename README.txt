CC0 Media Library
=================

Offline media resources. Version 1 publishes music only: 118 unique original Ogg Vorbis recordings (256,956,282 audio bytes). No audio has been transcoded, trimmed, normalized or retagged. Stable track IDs and audio paths are retained. Original creator tags and embedded album art remain inside the unchanged audio files; no separate image resource is distributed.

Release: https://github.com/jfpx/cc0-media-library/releases/tag/music-v1
Versioned ZIP: https://github.com/jfpx/cc0-media-library/releases/download/music-v1/music-cc0.zip
Latest music ZIP: https://github.com/jfpx/cc0-media-library/releases/latest/download/music-cc0.zip
Resource index: https://raw.githubusercontent.com/jfpx/cc0-media-library/main/index.json
Catalog: https://raw.githubusercontent.com/jfpx/cc0-media-library/music-v1/music/v1/catalog.json
Manifest: https://raw.githubusercontent.com/jfpx/cc0-media-library/music-v1/music/v1/manifest.json

Only music releases will use the GitHub latest-release pointer. Future other media types use independent entries in index.json and versioned release URLs. No other media type is available or downloaded by this baseline.

Check music-cc0.zip against SHA256SUMS.txt before extraction. Extract into a folder such as Movies/CC0Music: the resulting layout is Movies/CC0Music/music/catalog.json and music/<mood>/<style>/*.ogg, with music/licenses/*.txt and music/manifest.json. ZIP paths are relative to the selected extraction root; do not flatten them. The catalog path fields are relative to that root. No APK, application source, tests or raw evidence are included.

This release is a resource baseline, not an app downloader implementation. The current app bundles its 118 tracks; external folder loading and one-click download are not enabled by this release. A future integration may let the user grant read-only Android Storage Access Framework access to the extraction root; these are layout instructions, not a current app feature.

Metadata contract
-----------------
index.json schemaVersion=1 contains an extensible resources array. Each resource has an explicit type, version, catalog, manifest and archive with HTTPS URL, SHA-256 and byte count. Only type=music is present.
music/v1/catalog.json is the versioned public catalog; the identical bytes appear as music/catalog.json inside the ZIP. Track fields are explicitly allowlisted; private evidence and arbitrary runtime fields are omitted. IDs, hashes, sizes, titles, creators, categories, sample rates, channels, frames and whole-file loop boundaries match the approved originals. durationMs is an integer approximation of frames/sampleRate. licenseFile points to public notices. source is a public creator page. sourceSha256 equals sha256 because audio bytes are unchanged. creatorTags are retained only when supplied. playbackKind is retained when supplied; its absence on two legacy entries does not establish a loop claim. creator-loop records intent, not verified seamlessness; composition-repeat means repeating the whole composition. perceptuallyVerified is always false.
music/manifest.json lists payload files (catalog, audio and notices) with hashes and sizes; it excludes itself to avoid a circular hash. Its own hash and the complete ZIP hash are in the resource index. Repository music/v1/manifest.json has identical bytes. The archive fileCount and uncompressedBytes include that manifest. Consumers should enforce path, count, byte-size and hash limits before accepting files.

Rights and credits
------------------
CC0 applies only to rights the affirmer holds and can waive or license. Creator declarations are provenance, not an independent guarantee of worldwide rights or third-party clearance. Patent, trademark, privacy, publicity and other third-party rights may remain. No warranty or endorsement is implied. No listening-based, musicological or perceptual seamless-loop certification has been performed.

Although permitted within the license terms, Abstraction and Tallbeard Studios do not endorse the use of these assets in any projects relating to NFTs, AI/Machine Learning, or direct resale of unmodified assets.
This is non-endorsement, not an added CC0 restriction.

Creators: isaiah658; Igor Gundarev; yd; DJ CrisP; Abstraction / Tallbeard Studios (Benjamin Burnes). See per-track source URLs and licenseFile notices. The complete CC0 1.0 legal text is in music/licenses/CC0-1.0.txt. Original Abstraction pack notices are retained byte-for-byte. Newly assembled catalog and documentation are offered under CC0-1.0 to the extent of the compiler's rights, without changing creator rights or claiming universal clearance.
