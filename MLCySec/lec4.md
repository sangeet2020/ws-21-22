# Lecture 4
## Adversarial ML: Evasion Attacks

- Exam dates? Not yet decided.
- NVIDIA's cybersecurity platform: MORPHEUS

## CNN
- Pooling layer
    - by pooling (e.g. max or averge) filter responses at different locations we gain robustness to the exact spatial location of features.
- Characteristics of convnets
    - Feed forward
        - convolve input
        - no-linearity
        - pooling
    - Supervised
    - Train CNN by backpropagating classification error
- Fully connected layer
    - `32X32X3 -> stretch to 3072X1`
- convolutional layer
    - `32X32X3`: preseve spatial feature
    - Apply: `5X5X3` filter
    - convolve the filter with the image ie. slide over the image spatially, computing dot products.
    - The 3rd dimension `3` of the image should always match with the filte's 3rd dimension.
    - Apply multiple such filters each learning different features of the input image
    - convolve (slide) overall  spatiallocations
    - Size of each activation map: `28X28X1`
    - After applying 6 filter, total size of activation map: `28X28X6`
- Transfer learning
    -  knowledge gained while learning to recognize cars could apply when trying to recognize trucks
    - storing knowldge gained while solving one problem and applying it to different but related problem.
    - Finetuning
        - use lots of data for Proxy task and attain a local minima
        - further, use little data i.e. relevant to the target task and traina few more steps to achice next local minima to complete training to expose your new data to the model and learn features of it.
    

## Adversarial ML: Evasion Attacks
- Misleading an AI by manipulating the data during training
- ML is becoming ubiquitious in many products, part of IT infrastruture, part of defence mechanisms, part of attack surface
- Terminology
    - Influence
        - Causative Attacks
            - Affect training process
                - Offline learning
                - online learning
        - Exploratory attacks
            - Post training phase/ test time
            - explore adversarial space to change outcomes
                - systematic
                - Brute force fuzzing
            - continiously query the model to understand the mechanisms
    - Specificity
        - Direct/Targeted
        - indiscriminant attack
    - Security violation
        - integrity attacks
        - availability attack
        - causing the system to malfunction
        - attack system by overloading it 
            
- Importance of Adversarial ML
    - ML part of both problem and solution

- CIA trade goals
    - Membership inference attacks: 
        - trying to infer information on the training data
        - only observing ip/op
    - Model inference attacks
        - trying to infer info about the model
    - Reduce
        - Qality, performance, access (denial of service)
    - Manipulating
        - training data: poisionous attack
        - test data: evasion attack

## Evasion attacks
- robustness of ML
    - difficult to test in real world
    - Real world data
    - Human crafted/manipulated data
- Adversarial manipulation of input
    - Adding a perturbation makes the classifier to classiy into bogus labels.
    - eg. Schoolbus + perturbation (attack by attacker, added onto the image)-> Ostrich
- Spam Email example: has been shown to work for all kind of input
- L0 norm (change of dimension), L2 norm, L_infinity_form (largest change)
- Binary classifer Evasion attack
    - Linear classifier/logistic regression
    - find direction with strongest change
- Emperical Risk min.
    - inner maximization finds adversarial versions with high loss
    - outer minimization tries to find parameters so that adversarial loss of inner attack is minimized.
    - the attacker will try to maximize the loss by finding the best delta ($\delta$)
- Fast signed gradient method (**)
    - attacker wants to attack the model
    - compute gradient in the input domain in step and add this to the input image
    - changing input to maximize the loss
- Calini/Wagner cleaver attacks