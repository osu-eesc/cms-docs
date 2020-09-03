# Tips for banner images on the Extension website

Banner images display on county, program, and project pages across the full width of the top of the page. These images are very short and wide, and how exactly they are cropped depends on the size of the screen the visitor is using. Here are some tips for choosing and uploading photos that work well as banner images.

## General tips

  - **Crop the image to 2000px wide by 325px tall before you upload it.** This gives you more control over how the image is cropped, which otherwise the system would do automatically.
  - **Use the focal point control for the image to further control cropping.** You can choose a specific point on the image to serve as a “focal point” that will always be included when the image is cropped by the system. To change the focal point, edit the page where the banner images is uploaded and click the “Edit” button for the banner image. In the window that appears, there is a small crosshairs icon on the image preview. Click and drag the crosshairs to the desired focal point and save.

## Types of images that work well

- **Landscapes that include the horizon**
    - Examples: [Harney County](https://extension.oregonstate.edu/harney), [KBREC](https://extension.oregonstate.edu/kbrec), [SOREC](https://extension.oregonstate.edu/sorec), [Hemp](https://extension.oregonstate.edu/crop-production/hemp), [Commercial Fishing](https://extension.oregonstate.edu/animals-livestock/fishing)
- **Aerial views of a landscape**
    - Examples: [Umatilla County Milton-Freewater](https://extension.oregonstate.edu/umatilla-mf), [Union County](https://extension.oregonstate.edu/union)
- **Group photos with one or two rows of people lined up**
    - Examples: [Tillamook County](https://extension.oregonstate.edu/tillamook), [Deschutes Co. 4-H](https://extension.oregonstate.edu/4h/deschutes), [Lane Co. 4-H](https://extension.oregonstate.edu/4h/lane), [Sherman Co. 4-H](https://extension.oregonstate.edu/4h/sherman)
- **Photos containing multiple people or animals where their heads are lined up horizontally**
    - Livestock herds: [Pasture and forages](https://extension.oregonstate.edu/crop-production/pastures-forages), [Dairy](https://extension.oregonstate.edu/animals-livestock/dairy), [Horses](https://extension.oregonstate.edu/animals-livestock/horses),  [Swine](https://extension.oregonstate.edu/animals-livestock/swine)
    - 4-H members at fair: [Malheur Co. 4-H](https://extension.oregonstate.edu/4h/malheur), [Union Co. 4-H](https://extension.oregonstate.edu/4h/union)
    - Misc. examples: [Land Steward Program](https://extension.oregonstate.edu/land-steward), [Lincoln Co. MG](https://extension.oregonstate.edu/mg/lincoln), [Jefferson Co. 4-H](https://extension.oregonstate.edu/4h/jefferson), [Physical Activity](https://extension.oregonstate.edu/families-health/physical-activity)
- **Close-up photos of a texture or pattern**
    - Leaves and trees: [Benton County](https://extension.oregonstate.edu/benton), [Lane County](https://extension.oregonstate.edu/lane),  [Lawn and turfgrass](https://extension.oregonstate.edu/gardening/lawn), [Christmas trees](https://extension.oregonstate.edu/forests/christmas-trees)
    - Flowers:  [Linn-Benton MG](https://extension.oregonstate.edu/mg/linn-benton), [Columbia Co. MG](https://extension.oregonstate.edu/mg/columbia), [Agritourism](https://extension.oregonstate.edu/community-vitality/agritourism)
    - Produce: [Berries and fruit](https://extension.oregonstate.edu/gardening/berries-fruit), [Hazelnuts and nut crops](https://extension.oregonstate.edu/crop-production/nuts), [Umatilla Co. MG](https://extension.oregonstate.edu/mg/umatilla)
    - Food: [Clackamas Co. 4-H](https://extension.oregonstate.edu/4h/clackamas), [Commercial food processing](https://extension.oregonstate.edu/food/processing),  [Local/regional/community food systems](https://extension.oregonstate.edu/food/food-systems)
    - Bees and honeycombs: [Bees and pollinators](https://extension.oregonstate.edu/gardening/pollinators), [Master Beekeeper](https://extension.oregonstate.edu/mb)
- **Photos of signage or other decorations/features of a location** (don’t include text that you want people to read, it might get cut off on smaller screens)
    - Signage and location features: [Clatsop County](https://extension.oregonstate.edu/clatsop), [Columbia County](https://extension.oregonstate.edu/columbia), [Polk Co. MG](https://extension.oregonstate.edu/mg/polk), [OSU Portland Center](https://extension.oregonstate.edu/portland-center)
    - Branded objects/decorations: [Lincoln County](https://extension.oregonstate.edu/lincoln), [4-H (statewide)](https://extension.oregonstate.edu/4h), [Benton Co. 4-H](https://extension.oregonstate.edu/4h/benton)
- **Posed/“still life” photos of relevant objects**
    - Examples: [Home food safety and preservation](https://extension.oregonstate.edu/mfp), [Family emergency preparedness](https://extension.oregonstate.edu/families-health/emergency-prep), [Wine/beer/cider/spirits](https://extension.oregonstate.edu/food/wine-beer), [Finance/budgeting/taxes](https://extension.oregonstate.edu/business-economics/finance)

## Technical details

The following are technical details about how the system handles/generates banner images.

1.	User uploads photo and system saves the original version.
2.	When user saves photo, system generates cropped version (2000px X 325px) from the original uploaded file based on the focal point set for the image.
    1.	Focal point is a set of two numbers (x, y), where x represents the horizontal position of the point as a percentage of the total width of the image (i.e. x=50 -> exactly halfway horizontally across the image, from the left) and y represents the vertical position of the point as a percentage of the total height of the image (i.e. y=50 -> exactly halfway vertically across the image, from the top).
    2.	When a focal point (x,y ) is set, the system uses the following process to crop an image:
        1.	Create a box the size the cropped image will be (in this case 2000px X 325px).
        2.	Identify the point in the box x% across horizontally and y% across vertically.
        3.	Resize the original image so that it is as close to the size of the box as possible while still covering it completely.
        4.	Identify the point in the resized image x% across horizontally and y% across vertically.
        5.	Lay the box on top of the resized image so that the two identified points are exactly on top of each other.
        6.	Delete all of the resized image that is outside the box.
        7.	The cropped image is what’s left behind under the box.
    3.	Note that you can skip this cropping step by manually resizing and cropping the image before you upload it.
3.	When a visitor views a page with a banner image, their web browser has to crop it in order to be exactly the width of their screen. It will use the same process as in step 2b above, except the size of the Box is not constant, it depends on the device the visitor is using.
