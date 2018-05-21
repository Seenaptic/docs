.. seenaptic documentation master file, created by
   sphinx-quickstart on Mon May 21 11:31:35 2018.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to seenaptic's documentation!
=========================================

.. toctree::
   :maxdepth: 2
   :caption: Contents:

So this should show some php code::

  {"test":"ok"}

What about PHP ?

.. code-block:: php

  return $i*2;

Or javascript

.. code-block:: javascript

  for (var i = 0; i< Math.min(emrchs.length,30); i++){
  var elem = merchs[i];
  if(elem.getAttribute('data-merch-arbo')!="mega_menu")//temporairement on ne déclenche pas d'impression pour le menu
  {
    var promoId = elem.getAttribute('data-merch-arbo')+'::'+elem.getAttribute('data-merch-pos')+'::'+elem.getAttribute('data-merch-name');
    if(promos.indexOf(promoId) == -1){
      ga('lmfr.ec:addPromo',{'id':promoId,'name':elem.getAttribute('data-merch-arbo'), 'creative':elem.getAttribute('data-merch-name'),'position':elem.getAttribute('data-merch-pos')});
      promos.push(promoId);
    }
  }
  elem.addEventListener('click',function(){
    var target = elem;
    return function(e){
      elem = target;
      ga('lmfr.ec:addPromo',{'id':elem.getAttribute('data-merch-arbo')+'::'+elem.getAttribute('data-merch-pos')+'::'+elem.getAttribute('data-merch-name'),'name':elem.getAttribute('data-merch-arbo'), 'creative':elem.getAttribute('data-merch-name'),'position':elem.getAttribute('data-merch-pos')});
      ga('lmfr.ec:setAction', 'promo_click');
      ga('lmfr.send', 'event', 'Clic merchandising', elem.getAttribute('data-merch-arbo')+'::'+elem.getAttribute('data-merch-pos'), elem.getAttribute('data-merch-name'),{
        'dimension53':elem.getAttribute('data-merch-arbo'),
        'dimension54':elem.getAttribute('data-merch-pos')
      });
      window.localStorage.setItem('lastMerch',elem.getAttribute('data-merch-arbo')+'::'+elem.getAttribute('data-merch-pos')+'::'+elem.getAttribute('data-merch-name'));
      if(elem.getAttribute('data-merch-pos').indexOf('cross-sell') != -1)
        window.localStorage.setItem('lastOpeco',"cross-sell"); 
      else
        window.localStorage.setItem('lastOpeco',"Merchandising interne");  
    }}());
  }

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
