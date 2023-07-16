---

excalidraw-plugin: parsed
tags: [excalidraw]

---
==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠==


# Text Elements
program: <PATH to script>
method: bayes
metric:
  goal: maximize
  name: val_acc
early_terminate:
  type: hyperband
  min_iter: 10

parameters:
  training_params.initial_lr:
    distribution: uniform
    max: 0.5
    min: 0.001

  strassen_params.exexclude_layers:
    values: [['conv1'], ['conv1', 'layer1']

  training_params.optimizer_params.weight_decay:
    distribution: uniform
    min: 1e-5
    max: 1e-2


command:
  - ${env}
  - python
  - ${program}
  - ${args_no_hyphens} ^pCVJ7Blk

sweep.yaml ^Yh5ssCbM

[random, grid] ^XDpXAbsA

import wandb

# Pass your defaults to wandb.init
wandb.init(config=cfg)




 ^jkHcGtWQ

script.py ^5MvQgcAp

wandb sweep --project <wandb project> sweep.yaml
 ^h7XCMsLr

CLI from every agent ^jF2EiAp5

CLI from single machine ^cTexUhUU

wandb agent autonac/strassennets_cifar/nehy2nx3 ^CkKXoljP

 ^AgBmKiqT


# Embedded files
6ac993f7586a4c83859dd4743fe67bfb9d591d5a: $$\textrm{sweep params} \subseteq \textrm{cfg}$$
8819e9566f0886d17d3b9d78e2836d4f6a5ff43c: [[Pasted Image 20220626121437_238.png]]
fa604da1582e71d80ff39fdcf0e5d482cccd8de4: [[Pasted Image 20220626122235_141.png]]

%%
# Drawing
```json
{
	"type": "excalidraw",
	"version": 2,
	"source": "https://github.com/zsviczian/obsidian-excalidraw-plugin/releases/tag/1.9.7",
	"elements": [
		{
			"type": "text",
			"version": 304,
			"versionNonce": 738955056,
			"isDeleted": false,
			"id": "pCVJ7Blk",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -573.6133766174316,
			"y": -259.7293243408203,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 378.5625,
			"height": 468.5455567998623,
			"seed": 14722512,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1656248906807,
			"link": null,
			"locked": false,
			"fontSize": 13.46395278160524,
			"fontFamily": 3,
			"text": "program: <PATH to script>\nmethod: bayes\nmetric:\n  goal: maximize\n  name: val_acc\nearly_terminate:\n  type: hyperband\n  min_iter: 10\n\nparameters:\n  training_params.initial_lr:\n    distribution: uniform\n    max: 0.5\n    min: 0.001\n\n  strassen_params.exexclude_layers:\n    values: [['conv1'], ['conv1', 'layer1']\n\n  training_params.optimizer_params.weight_decay:\n    distribution: uniform\n    min: 1e-5\n    max: 1e-2\n\n\ncommand:\n  - ${env}\n  - python\n  - ${program}\n  - ${args_no_hyphens}",
			"rawText": "program: <PATH to script>\nmethod: bayes\nmetric:\n  goal: maximize\n  name: val_acc\nearly_terminate:\n  type: hyperband\n  min_iter: 10\n\nparameters:\n  training_params.initial_lr:\n    distribution: uniform\n    max: 0.5\n    min: 0.001\n\n  strassen_params.exexclude_layers:\n    values: [['conv1'], ['conv1', 'layer1']\n\n  training_params.optimizer_params.weight_decay:\n    distribution: uniform\n    min: 1e-5\n    max: 1e-2\n\n\ncommand:\n  - ${env}\n  - python\n  - ${program}\n  - ${args_no_hyphens}",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "program: <PATH to script>\nmethod: bayes\nmetric:\n  goal: maximize\n  name: val_acc\nearly_terminate:\n  type: hyperband\n  min_iter: 10\n\nparameters:\n  training_params.initial_lr:\n    distribution: uniform\n    max: 0.5\n    min: 0.001\n\n  strassen_params.exexclude_layers:\n    values: [['conv1'], ['conv1', 'layer1']\n\n  training_params.optimizer_params.weight_decay:\n    distribution: uniform\n    min: 1e-5\n    max: 1e-2\n\n\ncommand:\n  - ${env}\n  - python\n  - ${program}\n  - ${args_no_hyphens}",
			"lineHeight": 1.2,
			"baseline": 465
		},
		{
			"type": "text",
			"version": 268,
			"versionNonce": 717351376,
			"isDeleted": false,
			"id": "Yh5ssCbM",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -538.0473976135254,
			"y": -307.57899475097656,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 117.1875,
			"height": 24,
			"seed": 451017520,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1656236180077,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 3,
			"text": "sweep.yaml",
			"rawText": "sweep.yaml",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "sweep.yaml",
			"lineHeight": 1.2,
			"baseline": 19
		},
		{
			"type": "arrow",
			"version": 425,
			"versionNonce": 1241930544,
			"isDeleted": false,
			"id": "He4ivsAZVTac7u0-caE_B",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -460.12019212155684,
			"y": -235.81175047597765,
			"strokeColor": "#1864ab",
			"backgroundColor": "transparent",
			"width": 320.99784333615645,
			"height": 0.9492944382367341,
			"seed": 105608144,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1656236180077,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": {
				"elementId": "XDpXAbsA",
				"focus": 0.03724572324512112,
				"gap": 12.45526123046875
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					320.99784333615645,
					-0.9492944382367341
				]
			]
		},
		{
			"type": "text",
			"version": 51,
			"versionNonce": 75771856,
			"isDeleted": false,
			"id": "XDpXAbsA",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -126.66708755493164,
			"y": -248.59286499023438,
			"strokeColor": "#1864ab",
			"backgroundColor": "transparent",
			"width": 164.0625,
			"height": 24,
			"seed": 1617956656,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "He4ivsAZVTac7u0-caE_B",
					"type": "arrow"
				}
			],
			"updated": 1656236180077,
			"link": null,
			"locked": false,
			"customData": {
				"legacyTextWrap": true
			},
			"fontSize": 20,
			"fontFamily": 3,
			"text": "[random, grid]",
			"rawText": "[random, grid]",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "[random, grid]",
			"lineHeight": 1.2,
			"baseline": 19
		},
		{
			"type": "rectangle",
			"version": 331,
			"versionNonce": 1338069512,
			"isDeleted": false,
			"id": "AsOWb-I6gHPDrYe3rv_l7",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -608.8495826721191,
			"y": -261.5740661621094,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 402.74741617838544,
			"height": 524.1921539306642,
			"seed": 721784112,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1689485124874,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 973,
			"versionNonce": 973977040,
			"isDeleted": false,
			"id": "jkHcGtWQ",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 118.87893295288086,
			"y": -253.439453125,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 285.08203125,
			"height": 154.638857954402,
			"seed": 1283696944,
			"groupIds": [
				"QDDBrJ5D_JiJ6GDKZpKo-"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1656236180078,
			"link": null,
			"locked": false,
			"fontSize": 14.31841277355574,
			"fontFamily": 3,
			"text": "import wandb\n\n# Pass your defaults to wandb.init\nwandb.init(config=cfg)\n\n\n\n\n",
			"rawText": "import wandb\n\n# Pass your defaults to wandb.init\nwandb.init(config=cfg)\n\n\n\n\n",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "import wandb\n\n# Pass your defaults to wandb.init\nwandb.init(config=cfg)\n\n\n\n\n",
			"lineHeight": 1.2,
			"baseline": 151
		},
		{
			"type": "rectangle",
			"version": 576,
			"versionNonce": 2133675824,
			"isDeleted": false,
			"id": "VErm7qJxRbkTyy9CPrDCf",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 105.29238510131836,
			"y": -262.3285369873047,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 314.44921875,
			"height": 106.413818359375,
			"seed": 834576688,
			"groupIds": [
				"QDDBrJ5D_JiJ6GDKZpKo-"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1656236180078,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 504,
			"versionNonce": 1349942224,
			"isDeleted": false,
			"id": "5MvQgcAp",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 152.17800521850586,
			"y": -305.3922576904297,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 105.46875,
			"height": 24,
			"seed": 2024618448,
			"groupIds": [
				"QDDBrJ5D_JiJ6GDKZpKo-"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1656236180078,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 3,
			"text": "script.py",
			"rawText": "script.py",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "script.py",
			"lineHeight": 1.2,
			"baseline": 19
		},
		{
			"type": "arrow",
			"version": 1104,
			"versionNonce": 1400217040,
			"isDeleted": false,
			"id": "aVyX-yqxyMwMertgheXjZ",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -483.1736183166504,
			"y": -102.94486999511719,
			"strokeColor": "#1864ab",
			"backgroundColor": "transparent",
			"width": 719.5471158498084,
			"height": 75.4036865234375,
			"seed": 1477156304,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1656249295758,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					412.3466898600261,
					-11.026265462239621
				],
				[
					719.5471158498084,
					-75.4036865234375
				]
			]
		},
		{
			"type": "image",
			"version": 2934,
			"versionNonce": 125704656,
			"isDeleted": false,
			"id": "dxj1TEIz",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 6.098423768830148,
			"x": -51.045494259154395,
			"y": -156.66731505208534,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 129.55158154548062,
			"height": 13.980386497713736,
			"seed": 29656,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1656250959578,
			"link": null,
			"locked": false,
			"status": "pending",
			"fileId": "6ac993f7586a4c83859dd4743fe67bfb9d591d5a",
			"scale": [
				1,
				1
			]
		},
		{
			"type": "text",
			"version": 599,
			"versionNonce": 1995009328,
			"isDeleted": false,
			"id": "h7XCMsLr",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -59.23636245727539,
			"y": 22.904067993164034,
			"strokeColor": "#e67700",
			"backgroundColor": "transparent",
			"width": 562.5,
			"height": 48,
			"seed": 732740048,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1656249241788,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 3,
			"text": "wandb sweep --project <wandb project> sweep.yaml\n",
			"rawText": "wandb sweep --project <wandb project> sweep.yaml\n",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "wandb sweep --project <wandb project> sweep.yaml\n",
			"lineHeight": 1.2,
			"baseline": 43
		},
		{
			"type": "rectangle",
			"version": 495,
			"versionNonce": 1486044624,
			"isDeleted": false,
			"id": "qyPuHuOOzaxiCtT9tZRbO",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -128.82614517211914,
			"y": 0.6549224853515341,
			"strokeColor": "#e67700",
			"backgroundColor": "transparent",
			"width": 679.5437622070312,
			"height": 127.74139404296876,
			"seed": 1414708176,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1656249241788,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 495,
			"versionNonce": 609767376,
			"isDeleted": false,
			"id": "cTexUhUU",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -53.92288589477539,
			"y": -62.133205241985195,
			"strokeColor": "#e67700",
			"backgroundColor": "transparent",
			"width": 375.3148193359375,
			"height": 40.937887655722164,
			"seed": 1664483792,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1656249245763,
			"link": null,
			"locked": false,
			"fontSize": 32.75031012457773,
			"fontFamily": 1,
			"text": "CLI from single machine",
			"rawText": "CLI from single machine",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "CLI from single machine",
			"lineHeight": 1.25,
			"baseline": 29
		},
		{
			"type": "image",
			"version": 210,
			"versionNonce": 2128367056,
			"isDeleted": false,
			"id": "2iAEmEWDfQTr0aN4GDkeE",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -393.6279945373535,
			"y": -358.69645002885295,
			"strokeColor": "transparent",
			"backgroundColor": "transparent",
			"width": 131.35409545898435,
			"height": 87.4101798872514,
			"seed": 123739952,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1656236180078,
			"link": null,
			"locked": false,
			"status": "pending",
			"fileId": "8819e9566f0886d17d3b9d78e2836d4f6a5ff43c",
			"scale": [
				1,
				1
			]
		},
		{
			"type": "image",
			"version": 536,
			"versionNonce": 640956208,
			"isDeleted": false,
			"id": "OQq1qQvI-G5Ubum6FMKF3",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -88.37309646606445,
			"y": 53.71997747421261,
			"strokeColor": "transparent",
			"backgroundColor": "transparent",
			"width": 608.7926788330078,
			"height": 56.22876825332642,
			"seed": 1029525296,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1656236180078,
			"link": null,
			"locked": false,
			"status": "pending",
			"fileId": "fa604da1582e71d80ff39fdcf0e5d482cccd8de4",
			"scale": [
				1,
				1
			]
		},
		{
			"type": "text",
			"version": 529,
			"versionNonce": 463750960,
			"isDeleted": false,
			"id": "jF2EiAp5",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 28.02529525756836,
			"y": 151.86962272025437,
			"strokeColor": "#e67700",
			"backgroundColor": "transparent",
			"width": 348.9183654785156,
			"height": 40.937887655722164,
			"seed": 1057647408,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1656249241788,
			"link": null,
			"locked": false,
			"fontSize": 32.75031012457773,
			"fontFamily": 1,
			"text": "CLI from every agent",
			"rawText": "CLI from every agent",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "CLI from every agent",
			"lineHeight": 1.25,
			"baseline": 29
		},
		{
			"type": "rectangle",
			"version": 612,
			"versionNonce": 353043408,
			"isDeleted": false,
			"id": "fdNmSn8loxPCnFjQxQ5m5",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -102.43228530883789,
			"y": 212.51307678222656,
			"strokeColor": "#e67700",
			"backgroundColor": "transparent",
			"width": 679.5437622070312,
			"height": 62.745056152343764,
			"seed": 814835504,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1656249241788,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 197,
			"versionNonce": 1475600688,
			"isDeleted": false,
			"id": "CkKXoljP",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -45.74881362915039,
			"y": 234.56398010253906,
			"strokeColor": "#e67700",
			"backgroundColor": "transparent",
			"width": 550.78125,
			"height": 24,
			"seed": 926223152,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1656249241788,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 3,
			"text": "wandb agent autonac/strassennets_cifar/nehy2nx3",
			"rawText": "wandb agent autonac/strassennets_cifar/nehy2nx3",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "wandb agent autonac/strassennets_cifar/nehy2nx3",
			"lineHeight": 1.2,
			"baseline": 19
		},
		{
			"type": "text",
			"version": 5,
			"versionNonce": 2074011088,
			"isDeleted": false,
			"id": "AgBmKiqT",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 77.23070526123047,
			"y": -394.5172008445046,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 11.71875,
			"height": 24,
			"seed": 1901243856,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1656236180079,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 3,
			"text": "",
			"rawText": "",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "",
			"lineHeight": 1.2,
			"baseline": 19
		}
	],
	"appState": {
		"theme": "dark",
		"viewBackgroundColor": "#ffffff",
		"currentItemStrokeColor": "#e67700",
		"currentItemBackgroundColor": "transparent",
		"currentItemFillStyle": "hachure",
		"currentItemStrokeWidth": 1,
		"currentItemStrokeStyle": "solid",
		"currentItemRoughness": 1,
		"currentItemOpacity": 100,
		"currentItemFontFamily": 3,
		"currentItemFontSize": 20,
		"currentItemTextAlign": "left",
		"currentItemStartArrowhead": null,
		"currentItemEndArrowhead": "arrow",
		"scrollX": 666.7045224507649,
		"scrollY": 569.3517222687692,
		"zoom": {
			"value": 0.6000000000000001
		},
		"currentItemRoundness": "round",
		"gridSize": null,
		"colorPalette": {},
		"currentStrokeOptions": null,
		"previousGridSize": null
	},
	"files": {}
}
```
%%