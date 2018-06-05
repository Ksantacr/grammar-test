{
  "GrammarRulesList": [
    {
      "RuleId": "Person",
      "RuleElements": [
        {
          "RuleItems": "I|you|he|she"
        }
      ]
    },
    {
      "RuleId": "Action",
      "RuleElements": [
        {
          "RuleItems": "ate|bought|saw|sold|wanted"
        }
      ]
    },
    {
      "RuleId": "frase",
      "RuleElements": [
        {
          "RuleItems": "the|a|an"
        }
      ]
    },
    {
      "RuleId": "Food",
      "RuleElements": [
        {
          "RuleItems": "apple|manzana",
          "RuleReturnValue": "AP"
        },
        {
          "RuleItems": "banana|guineo",
          "RuleReturnValue": "BN"
        },
        {
          "RuleItems": "pear|pera",
          "RuleReturnValue": "PR"
        },
        {
          "RuleItems": "melon",
          "RuleReturnValue": "ML"
        }
      ]
    },
    {
      "RuleId": "Action2",
      "RuleElements": [
        {
          "RuleItems": "prueba|test|ejemplo"
        }
      ]
    },
    {
      "RuleId": "Demo2",
      "RuleElements": [
        {
          "RuleItems": "carro|moto|bus",
          "RuleReturnValue": "Motorizado"
        },
        {
          "RuleItems": "bicicleta|triciclo|patineta|patines",
          "RuleReturnValue": "NoMotorizado"
        }
      ]
    },
    {
      "RuleId": "Action3",
      "RuleElements": [
        {
          "RuleItems": "prueba|test|ejemplo"
        }
      ]
    }
  ],
  "GrammarRulesRefList": [
    [
      {
        "Type": "Fix",
        "RuleId": "Person",
        "RuleRefElements": [
          {
            "NodeText": "Yo"
          }
        ]
      },
      {
        "Type": "Fix",
        "RuleId": "Action",
        "RuleRefElements": [
          {
            "NodeText": "ate"
          }
        ]
      },
      {
        "Type": "Opt",
        "RuleId": "frase",
        "RuleRefElements": [
          {
            "NodeText": "the"
          }
        ]
      },
      {
        "Type": "Out",
        "RuleId": "Food",
        "RuleRefElements": [
          {
          	"ImplicationMode": "B",
            "NodeText": "apple",
            "ImplicationsList": [
              {
                "RuleRefName": "Food"
              }
              ]
          }
        ]
      },
      {
        "Type": "Grb",
        "RuleId": "Grb",
        "RuleRefElements": []
      }
    ],
    [
      {
        "Type": "Fix",
        "RuleId": "Action2",
        "RuleRefElements": [
          {
            "NodeText": "test"
          }
        ]
      },
      {
        "Type": "Out",
        "RuleId": "Demo2",
        "RuleRefElements": [
    	  {
			"ImplicationMode": "B",
			"NodeText": "vehiculo",
			"ImplicationsList": [
              {
                "RuleRefName": "Demo2"
              }
              ]
		},
		{
			"ImplicationMode": "I",
			"NodeText": "sin_motor",
			"ImplicationsList": [
              {
                "RuleRefName": "Demo2",
                "ImplicationValue": "NoMotorizado"
              },
              {
                "RuleRefName": "Food",
                "ImplicationValue": "AP"
              }
            ]
			},
          {
          	"ImplicationMode": "I",
            "NodeText": "con_motor",
            "ImplicationsList": [
              {
                "RuleRefName": "Demo2",
                "ImplicationValue": "Motorizado"
              }
              ]
          }
        ]
      },
      {
        "Type": "Grb",
        "RuleId": "Grb",
        "RuleRefElements": []
      }
    ]
  ],
  "GrammarFileName": "TestGrm02"
}
