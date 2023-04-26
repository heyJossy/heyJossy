ggplot(dplyr::arrange(df,freq),
           aes(label = word,size=freq,color = -log10(p.adjust),angle = angle)) +
  geom_text_wordcloud(rm_outside = TRUE,eccentricity = 1,shape = "square") +
  scale_size_area(max_size = 16)+
  heme_minimal()+theme(aspect.ratio =  0.7)
