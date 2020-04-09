color-corner.py
=========

```python
    f = corner.corner(nlposteriors[mask,2:], 
        labels= labels,
        bins=int(np.sqrt(nlposteriors.shape[0])), 
        range= ranges,
        #quantiles=(0.16, 0.84),
        plot_contours=False,
        plot_density=False,
        data_kwargs={
            'c':nlposteriors[mask,1],
            'vmin':np.percentile(nlposteriors[:,1],1),
            'vmax':np.percentile(nlposteriors[:,1],50),
            'cmap':newcmp,
        },
        label_kwargs={
            'labelpad':15,
        },
        hist_kwargs={
            'color':'black'
        }
    )
```

Examples:

![](color_posterior1.png)

![](color_posterior2.png)

Read the [original documentation](http://corner.readthedocs.io/)
