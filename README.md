# disinfo
## Repository for https://www.memelab.org/content/generating-disinformation-and-testing-its-coherence

This repo hosts code to generate conspiratorially-minded output from GPT2 as well as surveyed data testing the "coherence" of the output. `hysteria.txt` is the disinfo corpus, with `hysteria_qs.pdf` and `hysteria_answers.pdf` constituting the collected coherence datapoints. 

## Fine-tuning / generation parameters 

Once the model is loaded using the iPython notebook 

    gpt2.finetune(sess, dataset=file_name, model_name= '355M' , steps= 900, restore_from= 'latest' , run_name= 'run2' , print_every= 10 ,sample_every= 200 , save_every= 500 )
    
    gpt2.generate(sess, run_name= 'run3' , temperature= 1.3 , length= 600 , prefix= 'A new study' , truncate= 'illusions and lies.' , include_prefix= False )
