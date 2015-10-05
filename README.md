package com.publishing.services;

import java.util.Date;
import java.util.List;

import org.springframework.beans.factory.annotation.Autowired;

import com.publishing.dao.DataDao;
import com.publishing.model.Article;

public class DataServicesImpl implements DataServices {

	@Autowired
	DataDao dataDao;
	
	@Override
	public boolean addEntity(Article article) throws Exception {
		return dataDao.addEntity(article);
	}

	@Override
	public boolean updateEntity(Article article) throws Exception {
		return dataDao.updateEntity(article);
	}

	@Override
	public Article getEntityById(long id) throws Exception {
		return dataDao.getEntityById(id);
	}

	@Override
	public List<Article> getEntityList() throws Exception {
		return dataDao.getEntityList();
	}

	@Override
	public boolean deleteEntity(long id) throws Exception {
		return dataDao.deleteEntity(id);
	}

	@Override
	public List<Article> getEntityListByAuthor(String author) throws Exception {
		return dataDao.getEntityListByAuthor(author);
	}

	@Override
	public List<Article> getEntityListByKeyword(String keyword)
			throws Exception {
		return dataDao.getEntityListByKeyword(keyword);
	}

	@Override
	public List<Article> getEntityListByDateRange(Date fromDate, Date toDate)
			throws Exception {
		return dataDao.getEntityListByDateRange(fromDate, toDate);
	}

}
/Coments/
