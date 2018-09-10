# Asset Store Batch Mode

Provides an API for uploading Unity Asset Store packages in batch mode.

## Installation/usage

1. Grab and import the latest Asset Store tools [here](http://u3d.as/1sF).
2. Since this is an unofficial API, it's recommended to create a separate Unity account and password (ex: asset-store-api@example.com), and add that account to your publisher administration. Hopefully in the future this can be replaced with an API key.
3. Clone this repository into the AssetStoreTools/Editor folder.
4. Call Unity from the command line with `-executeMethod Thinksquirrel.ASBM.AssetStoreBatchMode.UploadAssetStorePackage`. Alternatively, call `UploadAssetStorePackage()` (or one of its overloads) from another script. Your package must be placed in draft mode manually or uploading is skipped.
5. For command line arguments, see AssetStoreBatchMode.cs.

## Known issues

1. Setting main assets are not implemented yet (root path is implemented).
2. Login can occasionally timeout. Exception handling isn't the best right now either (async exceptions are not caught and just sit there until a timeout)
3. I AM NOT RESPONSIBLE for any issues with your Unity packages. This script is fairly safe (it hooks into the C# Asset Store client that the Asset Store tools use), but this is an unsupported API and it may break without warning. Don't say I didn't warn you :)
