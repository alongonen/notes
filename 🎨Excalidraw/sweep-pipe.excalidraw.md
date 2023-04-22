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
	"source": "https://excalidraw.com",
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
			"width": 379,
			"height": 463,
			"seed": 14722512,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1656248906807,
			"link": null,
			"locked": false,
			"fontSize": 13.46395278160524,
			"fontFamily": 3,
			"text": "program: <PATH to script>\nmethod: bayes\nmetric:\n  goal: maximize\n  name: val_acc\nearly_terminate:\n  type: hyperband\n  min_iter: 10\n\nparameters:\n  training_params.initial_lr:\n    distribution: uniform\n    max: 0.5\n    min: 0.001\n\n  strassen_params.exexclude_layers:\n    values: [['conv1'], ['conv1', 'layer1']\n\n  training_params.optimizer_params.weight_decay:\n    distribution: uniform\n    min: 1e-5\n    max: 1e-2\n\n\ncommand:\n  - ${env}\n  - python\n  - ${program}\n  - ${args_no_hyphens}",
			"rawText": "program: <PATH to script>\nmethod: bayes\nmetric:\n  goal: maximize\n  name: val_acc\nearly_terminate:\n  type: hyperband\n  min_iter: 10\n\nparameters:\n  training_params.initial_lr:\n    distribution: uniform\n    max: 0.5\n    min: 0.001\n\n  strassen_params.exexclude_layers:\n    values: [['conv1'], ['conv1', 'layer1']\n\n  training_params.optimizer_params.weight_decay:\n    distribution: uniform\n    min: 1e-5\n    max: 1e-2\n\n\ncommand:\n  - ${env}\n  - python\n  - ${program}\n  - ${args_no_hyphens}",
			"baseline": 460,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "program: <PATH to script>\nmethod: bayes\nmetric:\n  goal: maximize\n  name: val_acc\nearly_terminate:\n  type: hyperband\n  min_iter: 10\n\nparameters:\n  training_params.initial_lr:\n    distribution: uniform\n    max: 0.5\n    min: 0.001\n\n  strassen_params.exexclude_layers:\n    values: [['conv1'], ['conv1', 'layer1']\n\n  training_params.optimizer_params.weight_decay:\n    distribution: uniform\n    min: 1e-5\n    max: 1e-2\n\n\ncommand:\n  - ${env}\n  - python\n  - ${program}\n  - ${args_no_hyphens}"
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
			"width": 118,
			"height": 24,
			"seed": 451017520,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1656236180077,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 3,
			"text": "sweep.yaml",
			"rawText": "sweep.yaml",
			"baseline": 19,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "sweep.yaml"
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
			"strokeSharpness": "round",
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
			"width": 165,
			"height": 24,
			"seed": 1617956656,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [
				{
					"id": "He4ivsAZVTac7u0-caE_B",
					"type": "arrow"
				}
			],
			"updated": 1656236180077,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 3,
			"text": "[random, grid]",
			"rawText": "[random, grid]",
			"baseline": 19,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "[random, grid]"
		},
		{
			"type": "rectangle",
			"version": 231,
			"versionNonce": 418608432,
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
			"width": 413.89111328125,
			"height": 518.8590545654297,
			"seed": 721784112,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1656236180078,
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
			"width": 285,
			"height": 151,
			"seed": 1283696944,
			"groupIds": [
				"QDDBrJ5D_JiJ6GDKZpKo-"
			],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1656236180078,
			"link": null,
			"locked": false,
			"fontSize": 14.31841277355574,
			"fontFamily": 3,
			"text": "import wandb\n\n# Pass your defaults to wandb.init\nwandb.init(config=cfg)\n\n\n\n\n",
			"rawText": "import wandb\n\n# Pass your defaults to wandb.init\nwandb.init(config=cfg)\n\n\n\n\n",
			"baseline": 148,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "import wandb\n\n# Pass your defaults to wandb.init\nwandb.init(config=cfg)\n\n\n\n\n"
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
			"strokeSharpness": "sharp",
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
			"width": 107,
			"height": 24,
			"seed": 2024618448,
			"groupIds": [
				"QDDBrJ5D_JiJ6GDKZpKo-"
			],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1656236180078,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 3,
			"text": "script.py",
			"rawText": "script.py",
			"baseline": 19,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "script.py"
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
			"strokeSharpness": "round",
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
			"x": -52.500016966671666,
			"y": -156.5137993237712,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 132.46062696051516,
			"height": 13.673355041085435,
			"seed": 29656,
			"groupIds": [],
			"strokeSharpness": "sharp",
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
			"width": 562,
			"height": 47,
			"seed": 732740048,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1656249241788,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 3,
			"text": "wandb sweep --project <wandb project> sweep.yaml\n",
			"rawText": "wandb sweep --project <wandb project> sweep.yaml\n",
			"baseline": 43,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "wandb sweep --project <wandb project> sweep.yaml\n"
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
			"strokeSharpness": "sharp",
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
			"width": 377,
			"height": 41,
			"seed": 1664483792,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1656249245763,
			"link": null,
			"locked": false,
			"fontSize": 32.75031012457773,
			"fontFamily": 1,
			"text": "CLI from single machine",
			"rawText": "CLI from single machine",
			"baseline": 29,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "CLI from single machine"
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
			"strokeSharpness": "round",
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
			"strokeSharpness": "round",
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
			"width": 350,
			"height": 41,
			"seed": 1057647408,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1656249241788,
			"link": null,
			"locked": false,
			"fontSize": 32.75031012457773,
			"fontFamily": 1,
			"text": "CLI from every agent",
			"rawText": "CLI from every agent",
			"baseline": 29,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "CLI from every agent"
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
			"strokeSharpness": "sharp",
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
			"width": 552,
			"height": 24,
			"seed": 926223152,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1656249241788,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 3,
			"text": "wandb agent autonac/strassennets_cifar/nehy2nx3",
			"rawText": "wandb agent autonac/strassennets_cifar/nehy2nx3",
			"baseline": 19,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "wandb agent autonac/strassennets_cifar/nehy2nx3"
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
			"width": 13,
			"height": 24,
			"seed": 1901243856,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1656236180079,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 3,
			"text": "",
			"rawText": "",
			"baseline": 19,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": ""
		},
		{
			"type": "line",
			"version": 3132,
			"versionNonce": 1417440048,
			"isDeleted": true,
			"id": "K4AhVV8eb5J0Y9jVdKMsY",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -127.01282152378094,
			"y": -372.84240868625386,
			"strokeColor": "#000000",
			"backgroundColor": "#82c91e",
			"width": 139.95088429585707,
			"height": 94.2901584639787,
			"seed": 764208,
			"groupIds": [
				"jf0yelQJGdeRHa8l9m_64",
				"c7tw7bgyBTrAKeQcdyx-I",
				"wKVhm-5_Fus1j1aPKW_xi"
			],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1656251098804,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					137.45176136200217,
					0.3296858687552004
				],
				[
					139.95088429585707,
					78.79492263248568
				],
				[
					116.95895330439446,
					93.6307867264683
				],
				[
					1.4994737603127652,
					94.2901584639787
				],
				[
					0,
					0
				]
			]
		},
		{
			"type": "line",
			"version": 919,
			"versionNonce": 272048080,
			"isDeleted": true,
			"id": "zpwkTJYq8tWz2oWokZ4PL",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 10.562693573931579,
			"y": -299.3526285729181,
			"strokeColor": "#343a40",
			"backgroundColor": "white",
			"width": 24.1523085200346,
			"height": 25.638604428959752,
			"seed": 381862352,
			"groupIds": [
				"c7tw7bgyBTrAKeQcdyx-I",
				"wKVhm-5_Fus1j1aPKW_xi"
			],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1656251098804,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					-22.666012611109114,
					-3.344165795081998
				],
				[
					-24.152308520034605,
					22.294438633877753
				],
				[
					0,
					0
				]
			]
		},
		{
			"type": "text",
			"version": 52,
			"versionNonce": 170362160,
			"isDeleted": true,
			"id": "rZCOIbjZ",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -99.41742706298828,
			"y": -341.5447887351296,
			"strokeColor": "#a61e4d",
			"backgroundColor": "transparent",
			"width": 13,
			"height": 24,
			"seed": 1999333328,
			"groupIds": [
				"wKVhm-5_Fus1j1aPKW_xi"
			],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1656251098804,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 3,
			"text": "",
			"rawText": "",
			"baseline": 19,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": ""
		},
		{
			"type": "text",
			"version": 193,
			"versionNonce": 836937168,
			"isDeleted": true,
			"id": "ZJbOUYNU",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -124.39996083577466,
			"y": -341.4688397037281,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 144,
			"height": 35,
			"seed": 347173168,
			"groupIds": [
				"wKVhm-5_Fus1j1aPKW_xi"
			],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1656251098804,
			"link": null,
			"locked": false,
			"fontSize": 14.467290378509354,
			"fontFamily": 3,
			"text": "random, bayes run\nforever",
			"rawText": "random, bayes run\nforever",
			"baseline": 32,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "random, bayes run\nforever"
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
		"currentItemStrokeSharpness": "sharp",
		"currentItemStartArrowhead": null,
		"currentItemEndArrowhead": "arrow",
		"currentItemLinearStrokeSharpness": "round",
		"gridSize": null,
		"colorPalette": {}
	},
	"files": {}
}
```
%%