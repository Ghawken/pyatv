# Ghawken/pyatv – `indigo` branch

Upstream `postlund/pyatv` master (v0.18.0, last commit 2026-06-19) plus open upstream PRs
used by the Indigo appleTV plugin. Version: `0.18.0.post1`.

| PR | Summary |
|----|---------|
| #2894 | Fix AirPlay PIN pairing on tvOS 27 (X-Apple-Client-Name) |
| #2920 | AirPlay: raise on pair-setup error TLVs instead of hanging at SETUP |
| #2945 | core: close protocols when connect fails (no leaked connections on retry) |
| #2911 | mdns: don't stop a unicast scan before results stabilize |
| #2930 | scan: ask for every service type in the zeroconf unicast fallback |
| #2936 | scan: skip service names zeroconf refuses instead of aborting |
| #2926 | mDNS: ignore truncated DNS headers |
| #2931 | mdns: group multicast responses per device, not per source address |
| #2939 | companion: raise when a response carries an error code |
| #2935 | companion: do not dispatch unknown volume |
| #2897 | mrp: handle NaN elapsed time when calculating position |
| #2924 | Preserve AirPlay remote control authentication errors |
| #2917 | mrp: report a HomePod stereo pair leader as powered on |
| #2850 | raop: fix read-side deadlock in PatchedIceCastClient |
| #2942 | airplay: zero-pad lower word when parsing features |
| #2907 | typing fix for devices/device_uids |
| #2909 | test fixtures for newer zeroconf |

Conflicts resolved by hand: #2894 vs #2920 (`airplay/auth/hap.py`), #2931 vs #2926 (`core/mdns.py`, tests).
Full test suite: 1316 passed, 6 skipped.

Update: `git fetch upstream && git checkout indigo && git merge upstream/master`, re-run tests,
bump `PATCH_VERSION` in `pyatv/const.py`.
