# BreakHis
adam_opt=Adam(lr=params["lr"], beta_1=params["beta_1"], beta_2=params['beta_2'], epsilon=None, decay=0.0, amsgrad=params['amsgrad'])
*******************************************************************************************************************
amsgrad': True, 'beta_1': 0.6, 'beta_2': 0.9, 'dropout': 0.5, 'lr': 1e-05
*******************************************************************************************************************
'amsgrad': False, 'beta_1': 0.7, 'beta_2': 0.995, 'dropout': 0.6, 'lr': 0.0001,
*******************************************************************************************************************
space = {
         'lr': hp.choice('lr',[0.001, 0.0001, 0.00001,0.000001]),
#          'dropout': hp.choice('dropout', [0.4, 0.5, 0.6, 0.7]),
#          'batch_size': hp.choice('batch_size', [64]),
#          'epochs': hp.choice('epochs', [15, 20, 25, 30, 50]),
#          'optimizer': hp.choice('optimizer',['sgd','adam','rmsprop']),
#          'optimizer': hp.choice('optimizer',['rmsprop']),
#          'optimizer': hp.choice('optimizer',['adam']),
         'beta_1':hp.choice('beta_1',[0.3,0.4,0.5,0.6,0.7,0.8]),
         'beta_2':hp.choice('beta_2',[0.99,0.995,0.7,0.8,0.9,0.999]),
         'decay':hp.choice('decay',[0.0, 0.004, 0.0001, 0.1, 0.3, 0.5]),
#          'momentum':hp.choice('momentum',[0.3,0.5,0.7,0.9,1]),
#          'amsgrad':hp.choice('amsgrad',[False,True]),
#          'nesterov':hp.choice('nesterov',[False,True]),
#          'rho':hp.choice('rho',[0.4,0.5,0.6,0.7,0.8,0.9,1]),
        }


    adam_opt = Adam(lr=1e-5, beta_1=0.9, beta_2=0.999, epsilon=1e-08, decay=params['decay'])

