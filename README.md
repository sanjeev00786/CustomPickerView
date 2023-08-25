# BottomSheetPickerViewController

`BottomSheetPickerViewController` is a reusable Swift component that provides a customizable bottom sheet picker view with various font and appearance options.

![Simulator Screen Shot - iPhone 14 Pro - 2023-08-25 at 14 49 26](https://github.com/sanjeev00786/CustomPickerView/assets/31886785/db7e2d5e-e269-4f88-b6b8-6614f54339d9)

## Features

- Display a bottom sheet picker view for user selection.
- Customize the appearance of the title, picker items, and button text.
- Provides the selected item to the delegate on done button tap.
- Smooth animation and intuitive user interaction.

## Usage

1. Add the `BottomSheetPickerViewController.swift` file to your project.
2. Create an instance of `BottomSheetPickerViewController` with the desired options:

```swift
let items = ["Option 1", "Option 2", "Option 3"]
let customTitleFont = UIFont(name: "Inter-Bold", size: 20)
let customPickerItemFont = UIFont(name: "Inter-Regular", size: 16)
let customButtonFont = UIFont(name: "Inter-SemiBold", size: 18)
let customSelectedPickerItemFont = UIFont(name: "Inter-Medium", size: 18)

let bottomSheetPicker = BottomSheetPickerViewController(
    items: items,
    titleFont: customTitleFont,
    pickerItemFont: customPickerItemFont,
    buttonFont: customButtonFont,
    selectedPickerItemFont: customSelectedPickerItemFont,
    title: "Select an Option"
)
bottomSheetPicker.delegate = self
present(bottomSheetPicker, animated: true, completion: nil)

1. Implement the BottomSheetPickerDelegate in your view controller:

extension YourViewController: BottomSheetPickerDelegate {
    func didSelectItem(_ item: String) {
        print("Selected item: \(item)")
    }

    func didTapDone() {
        print("Done button tapped")
    }
}
Customization

titleFont: Set the font for the title label.
pickerItemFont: Set the font for the picker items.
buttonFont: Set the font for the done button.
selectedPickerItemFont: Set the font for the selected picker item.
You can customize more appearance aspects by modifying the provided properties in BottomSheetPickerViewController.
Requirements

iOS 10.0+
Swift 5.0+
License

This project is licensed under the MIT License - see the LICENSE file for details.

