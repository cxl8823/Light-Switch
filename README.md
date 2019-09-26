# Light-Switch
//
//  ViewController.swift
//  Light
//
//  Created by Cheeun Lee on 9/24/19.
//  Copyright © 2019 Cheeun Lee. All rights reserved.
//

import UIKit

class ViewController: UIViewController {

    var lightOn = true
    var yellowLightOn = false
    @IBOutlet var buttonChange: UIButton!
    
    override func viewDidLoad() {
        super.viewDidLoad()
        updateUI()
       
    }

    @IBAction func buttonPressed(_ sender: Any) {
        lightOn = !lightOn
        updateUI()
    }
    
    @IBAction func yellowLightOn(_ sender: Any) {
        yellowLightOn = !yellowLightOn
        updateUI()
    }
    
    func updateUI() {
        if !lightOn  {
            view.backgroundColor = .black
        } else if yellowLightOn {
            view.backgroundColor = .yellow
        } else if !yellowLightOn{
            view.backgroundColor = .white
        }
   
    }
    
}
