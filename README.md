# HookPickerPicAndVideo
PhotoPicker (iOS 8.0 or later)
RedPickerBaseViewController* picker = [RedPickerBaseViewController new];     
picker.defaultAssetCollectionType = PHAssetCollectionSubtypeSmartAlbumUserLibrary;     
PHFetchOptions * fetchResoultOption = [[PHFetchOptions alloc]init];     
fetchResoultOption.predicate = [NSPredicate predicateWithFormat:@"mediaType = %d",PHAssetMediaTypeImage];     picker.assetsFetchOptions = fetchResoultOption;     
picker.delegate = self;     
[self presentViewController:picker animated:YES completion:nil];  




@protocol RedPickerViewControllerDelegate <NSObject>  - (void)assetsPickerController:(RedPickerBaseViewController *)picker didFinishPickingAssets:(NSArray *)assets;
